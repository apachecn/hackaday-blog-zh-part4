# 这些都在库中——使用动态加载构建一个插件系统

> 原文：<https://hackaday.com/2018/07/12/its-all-in-the-libs-building-a-plugin-system-using-dynamic-loading/>

共享库是我们最好的朋友，它可以扩展 C 程序的功能，而不用重新发明轮子。它们提供了导出函数、变量和其他符号的集合，我们可以在自己的程序中使用它们，就好像共享库的内容是我们代码的直接组成部分一样。使用这种库的通常方式是在编译时简单地链接它们，让链接器解析所有外部符号，并确保在创建我们的可执行文件时一切就绪。每当我们运行我们的可执行文件时，作为操作系统的一部分，加载程序将再次尝试解析所有的符号，并将每个需要的库连同我们的可执行文件一起加载到内存中。

但是，如果我们不想在编译时添加库，而是在运行时根据需要自己加载库，那该怎么办呢？我们可以让它的存在可选，并相应地调整程序的功能，而不是预先定义对库的依赖。嗯，我们可以用动态加载的概念来做到这一点。在本文中，我们将研究动态加载，如何使用它，以及如何使用它——包括构建我们自己的插件系统。但是首先，我们将仔细看看共享库并自己创建一个。

注意，在不同的架构上，一些细节可能会有所不同，这里的所有示例都集中在 x86_64 Linux 上，尽管主要原理在其他系统上应该是相同的，包括 ARM 上的 Linux(Raspberry Pi)和其他类似 Unix 的系统。

## 构建共享库

迈向动态可加载库的第一步是普通的共享库。共享库只是程序代码和数据的集合，并没有什么太神秘的地方。它们是 ELF 文件，就像常规的可执行文件一样，只是它们通常没有一个`main()`函数作为入口点，它们的符号以一种方式排列，任何其他程序或库都可以根据需要在它们自己的上下文中使用它们。为了这样安排它们，我们使用带有`-fPIC`选项的`gcc`来生成*位置无关代码*。将下面的代码放在一个文件`libfunction.c`中。

```

int double_me(int value)
{
    return value + value;
}

```

是的，这就是所有要做的，一个简单的函数`double_me()`，它将给定值加倍并返回。为了把它变成我们自己的共享库`libmylib.so`，我们首先把 C 文件编译成与位置无关的目标文件，然后把它链接成一个共享库:

```

$ gcc -c -fPIC libfunction.c
$ gcc -shared -o libmylib.so libfunction.o

```

当然，我们可以把它合并成一个对`gcc`的调用，避免中间对象文件。请注意，您可能想要添加一个带有`-Wl,-soname,`选项的 *[soname](https://en.wikipedia.org/wiki/Soname)* ，并向输出文件添加一些版本控制，但是为了简单起见，我们现在不考虑这些。

```

$ gcc -shared -fPIC -o libmylib.so libfunction.c

```

不管怎样，我们现在有了自己的共享库`libmylib.so`，所以让我们开始使用它吧。

```

// file main.c
#include <stdio.h>

// declare the function, ideally the library has a .h file for this
int double_me(int);

int main(void)                 
{
    int i;
    for (i = 1; i <= 10; i++) {
        // call our library function
        printf("%d doubled is %d\n", i, double_me(i));
    }
    return 0;
}

```

现在，我们只需要记住在编译文件时链接我们的库，并将我们当前的工作目录添加到路径列表中`gcc`以找到库。请记住，库文件名应该采用`lib*library_name*.so`的形式，然后通过`-l*library_name*`进行链接。

```

$ gcc -o main main.c -L. -lmylib

```

这应该让链接器高兴，并输出我们的`main`可执行文件。但是装载机呢？它会自动找到我们的库吗？

```

$ ./main
./main: error while loading shared libraries: libmylib.so: cannot open shared object file: No such file or directory

```

这是一个很大的错误，它表明告诉链接器(编译器套件的一部分)我们的库不会让加载器(操作系统的一部分)神奇地知道它的位置。为了找出需要什么库，以及加载程序解决这些依赖关系的情况，我们可以使用`ldd`命令。为了从加载器获得更多的调试输出，我们可以在调用我们的可执行文件时设置`LD_DEBUG=all`环境变量。

因此，为了让加载程序找到我们的库，我们必须告诉它在哪里查找，要么通过将正确的目录添加到`LD_LIBRARY_PATH`环境变量，要么通过将它添加到`/etc/ld.so.conf.d/`目录内的`/etc/ld.so.conf`中的`ldconfig`路径。现在让我们用环境变量来尝试一下。

```

$ LD_LIBRARY_PATH=.:$LD_LIBRARY_PATH ./main
1 doubled is 2
2 doubled is 4
...
10 doubled is 20
$

```

是的，加载程序现在会找到我们的库并成功运行可执行文件。

## 动态加载共享库

对于我们的下一个技巧，我们将使用动态加载在运行时将库读入我们的代码。一旦加载，我们可以在其中搜索符号并提取它们为指针，然后使用它们，就像库在第一位置被链接一样。Unix 和类 Unix 系统为此提供了`libdl`。让我们看看如何这样调用我们的`double_up()`函数。

```

// dynload.c
#include <stdio.h>
#include <dlfcn.h>

int main(void) {
    // handle for dynamic loading functions
    void *handle;

    // function pointer for the library's double_me() function
    int (*double_me)(int);

    // just a counter
    int i;

    // open our library ..hopefully
    if ( (handle = dlopen("./libmylib.so", RTLD_LAZY)) == NULL) {
        return 1;
    }

    // try to extract "double_me" symbol from the library
    double_me = dlsym(handle, "double_me");
    if (dlerror() != NULL) {
        dlclose(handle);
        return 2;
    }

    // use double_me() just like with a regularly linked library
    for (i = 1; i <= 10; i++) {
        printf("%d doubled is %d\n", i, double_me(i));
    }

    dlclose(handle);
    return 0;
}

```

我们尝试使用`dlopen()`函数加载我们的库，该函数在成功时返回一个通用指针句柄。然后，我们可以用`dlsym()`从库中找到并提取出`double_me`符号，并将之前返回的句柄传递给它。如果符号被找到，`dlsym()`返回它的地址作为`void *`，它可以被分配给一个(最好是匹配的)表示符号的指针类型。在我们的例子中，一个函数指针将一个`int`作为参数，并返回`int`，就像我们的`double_me()`函数一样。如果全部成功，我们就可以调用刚提取的`double_me()`函数，就好像它从一开始就在那里一样，输出也将是一样的。编译的时候记得对照`libdl`链接就行了。

```

$ gcc -o dynload dynload.c -ldl
$ ./dynload
1 doubled is 2
2 doubled is 4
...
10 doubled is 20
$

```

好了，我们不再在编译时链接，而是在运行时加载我们的库，在提取符号后，我们可以像以前一样使用它。不可否认，单独使用动态加载作为链接器的替代本身并没有太大的用处。动态加载更常见的用途是通过集成一个插件系统来扩展程序的核心功能，该插件系统允许用户根据需要添加外部组件。一个主要的例子是 Apache webserver，它有一个扩展的模块列表，可以根据需要单独添加。当然，这里我们将关注一种更简单的方法。

## 构建你自己的插件系统

就拿老小孩的游戏*电话*来说吧(或者中文密语、密语邮件、破电话等)。有人以一个信息开始，它在周围悄悄地传播，最后一个孩子说最初的信息应该是什么。嗯，这听起来像是一堆插件可以通过从一个插件向另一个插件传递消息来完成的事情，在我们进行的过程中会稍微弄乱数据。我们将编写运行电话系统的代码，任何人都可以贡献一个孩子/插件。

作为一个 API，让我们假设这个插件接受一个指向消息的指针和一个长度作为参数，并直接在内存中修改消息。让我们简单地称它为`process`，这样函数看起来就像`void process(char **, int)`。这是一个带有`process()`功能的插件，它将每隔一个字符设置为大写:

```

// file plugin-uppercase.c
include <ctype.h>

void process(char **message, int len)
{   
    int i;
    char *msg = *message;

    for (i = 1; i < len; i += 2) {
        msg[i] = toupper(msg[i]);
    }
}

```

让我们马上把它转换成一个`uppercase.plugin`文件，假设我们还有两个插件，`increase.plugin`增加它找到的每一个数字，`leet.plugin`使我们的消息就是:l337。

```

$ gcc -shared -fPIC -o uppercase.plugin plugin-uppercase.c
$ gcc -shared -fPIC -o increase.plugin plugin-increase.c
$ gcc -shared -fPIC -o leet.plugin leet-replace.c
$

```

我们的主程序会将一条消息作为第一个参数，并将任意数量的插件文件作为参数列表的其余部分。它将一个接一个地加载插件，通过它们的`process()`函数将消息从一个插件传递到另一个插件，然后打印出结果。(为了集中注意力，我们假装生活在一个完美的小世界里，在那里不会发生错误。)

```

// file telephone.c
#include <stdio.h>
#include <string.h>
#include <dlfcn.h>

int main(int argc, char **argv) {
    void *handle;
    void (*process)(char **, int);
    int index;

    if (argc < 3) {
        printf("usage: %s <message> <plugin> [,<plugin>,...]\n", argv[0]);
        return 1;
    }

    // argv[1] is the message, start from index 2 for the plugin list
    for (index = 2; index < argc; index++) {
        // open next plugin
        handle = dlopen(argv[index], RTLD_NOW);
        // extract the process() function
        process = dlsym(handle, "process");
        // call the process function, modifying argv[1] directly
        process(&argv[1], strlen(argv[1]));
        // close the plugin
        dlclose(handle);
    }

    // print the resulting message
    printf("%s\n", argv[1]);
    return 0;
}

```

就像以前一样，我们加载插件文件(一个动态加载的共享库)，提取我们需要的函数，并执行它——只是这一次是在一个循环中。所以我们来编译测试一下。

```

$ gcc -o telephone telephone.c -ldl
$ ./telephone "hello hackaday" ./uppercase.plugin
hElLo hAcKaDaY
$ ./telephone "hello hackaday" ./uppercase.plugin ./leet.plugin 
h3lL0 h4cK4D4Y
$ ./telephone "hello hackaday" ./uppercase.plugin ./leet.plugin ./increase.plugin 
h4lL1 h5cK5D5Y
$

```

正如所料，随着每个插件以他们自己的方式改变输入信息，插件的数量和顺序作为我们主程序的参数将影响最终的信息。作为数据处理示例，这可能算不上什么，但是相同的概念当然可以用于一些更有用的场景。如果你对完整的实现很好奇，[你可以在 GitHub](https://github.com/sgreg/dynamic-loading) 上找到它。还要注意，我们的主程序从来没有改变过，如果我们决定对其中一个插件进行调整，我们只需要重新编译那个插件。我们甚至可以在主程序中添加重新加载插件的机制，我们甚至不必重启主程序本身。

### Raspberry Pi GPIO 监控器

遵循相同原则的更有用的场景之一可能是监控 Raspberry Pi 上的 GPIO 引脚的程序。我们会有不同的插件来处理我们的主程序从 GPIOs 中读取的任何信息。每个插件都有一组可以实现的基本功能:一个用于插件设置阶段，一个用于处理每个 GPIOs 状态变化，一个用于在插件不再使用时将其拆除。一个插件可以处理一个引脚上的输入变化，以改变输出引脚的状态，另一个插件可以在一个特定的输入引脚变高时执行一些任务，第三个插件可以将所有状态变化写入日志文件。

最后，动态加载部分与前面的例子没有太大的不同，深入研究这样一个 GPIO 监视器的细节超出了本文的范围。然而，如果我们没有实现它，我们就不会提到它，所以在 GitHub 上也可以找到一个基本的 GPIO 监视器[。](https://github.com/sgreg/dynamic-loading)

## 从这里去哪里

有了动态加载，我们看到了编译时链接的另一种方法，它使得用外部库扩展程序的主要功能更加容易。虽然从库中提取符号会增加一点复杂性，但主要原则相当简单明了:打开一个库，从中提取符号，然后关闭它。然而，这种简单性也有它的缺点:为了通过动态加载来扩展程序的功能，我们需要事先知道我们能在加载的库或插件中找到什么。我们不能简单地添加一个全新的函数，并希望我们的程序会神奇地动态了解它。但是，如果您在设计核心程序时考虑到这些限制，动态加载将为您提供一种根据需要扩展功能的灵活方式。

请注意，我们已经打开了安全问题的潘多拉魔盒。如果任意外部函数可以在我们的主代码中运行，那么它的安全性取决于它动态链接的库。滥用这种信任是 [DLL 注入攻击](https://en.wikipedia.org/wiki/DLL_injection)或 [DLL 劫持](https://stackoverflow.com/questions/3623490/what-is-dll-hijacking)的基础。如果攻击者能够骗过操作系统，让它向调用程序提供可动态加载的库，他们就赢了。

因为动态加载需要操作系统的支持，所以这对于 8 位微控制器环境来说并不算什么。不过，你总是会有[函数指针](http://hackaday.com/2018/05/02/directly-executing-chunks-of-memory-function-pointers-in-c/)。

### 关于查找符号的一些单词

你可能会想，如果`dlsym()`可以解析动态加载文件中的符号，那么一定有办法首先找到可用的符号，也许可以得到它们的完整列表。嗯，是的，在[二进制文件描述符库](https://en.wikipedia.org/wiki/Binary_File_Descriptor_library) `libbfd`的帮助下，常见的`binutils`工具如`readelf`或`nm`就是这么做的。此外，我们的动态加载库`libdl`的 GNU 扩展提供了`dlinfo()`函数来获得关于加载文件的更多信息。在你进入那个兔子洞之前，推荐进一步阅读一些关于 ELF 文件格式的资料。