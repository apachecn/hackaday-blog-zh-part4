# 窥视可执行文件和库内部，使调试更容易

> 原文：<https://hackaday.com/2020/05/28/peeking-inside-executables-and-libraries-to-make-debugging-easier/>

乍一看，编译器生成的可执行文件和构建过程中使用的库似乎都不太容易访问。它们是使应用程序运行的黑盒，或者当你交给它“正确的”库文件时，使链接器高兴。也有很多不要太深入挖掘的地方，因为通常情况下事情会很顺利，不需要为这些额外的细节而烦恼。

事实上，可执行文件和库都包含了大量通常只被操作系统、工具链、调试器和类似工具使用的信息。无论这些文件是 Windows PE 格式、老式 Linux `a.out`还是现代的`.elf`格式，当开发过程中出现问题时，有时人们不得不拿出正确的工具来检查它们，以便理解正在发生的事情。

本文将主要关注 Linux 平台，尽管大部分内容也适用于 BSD 和 MacOS，在某种程度上也适用于 Windows。

## 打开黑盒

![](img/fb951bcacb89426842779673a7ba0114.png)

不管你在哪个平台上，可执行文件和库格式都有一些共同的部分。当然，还有包含实际指令的部分，以及包含所有文本字符串和常量值的部分，这些都是我们在编译代码之前放入代码中的。如果我们指示编译器生成调试符号，并告诉链接器保留这些符号，那么我们也将调试符号包含在它自己的部分中。我们将在本文的后面讨论这些问题。

在 Linux 和许多其他操作系统上常用的 [ELF](https://en.wikipedia.org/wiki/Executable_and_Linkable_Format) (可执行可链接格式)中，大致布局如下图。并非所有这些部分都是必需的，它们是否包含取决于创建可执行文件时选择了哪些选项。

使用[文件](https://linux.die.net/man/1/file)实用程序可以快速查看可执行文件的属性:

```
ELF 32-bit LSB shared object, Intel 80386, version 1 (GNU/Linux), dynamically linked, interpreter /lib/ld-linux.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=0558c7ef0f6845826d012b4ccc14948a2ffe8277, stripped
```

这个输出告诉我们，我们正在处理一个 32 位二进制文件，它是为 x86 体系结构编译的，使用了许多共享库，并且去掉了调试符号。

如果调试符号仍然存在，我们会得到:

```
ELF 32-bit LSB shared object, Intel 80386, version 1 (GNU/Linux), dynamically linked, interpreter /lib/ld-linux.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=0558c7ef0f6845826d012b4ccc14948a2ffe8277, with debug_info, not stripped

```

在这个特殊的例子中，我们处理的是在 Raspbian Buster for x86 上编译的二进制文件，这是一个 32 位版本的 Linux，因此所有文件都匹配。

对于一个 Windows 可执行文件，我们得到以下不太详细的输出:

```
PE32+ executable (GUI) x86-64, for MS Windows
```

这告诉我们，我们正在处理一个为 64 位 x86-64 架构编译的 PE (Windows)可执行文件。

在这一点上，你可能已经猜到了，库，无论是动态的还是共享的，都使用[相同的格式](https://en.wikipedia.org/wiki/Comparison_of_executable_file_formats)作为可执行文件，所以举例来说，当我们使用 *file* 命令时，在 Linux 上检查一个`.so`共享库文件将会生成几乎相同的输出。

## 分担责任

(桌面)操作系统独有的功能是在应用程序启动时加载动态(共享)库。这里假设所需的库存在于主机系统上，并且位于库加载程序(一个 OS 组件)的搜索路径中。库也可以被版本化以指示不同的修订。这通常通过文件名来实现，用通用名称(如`libfoo.so`)符号链接到实际文件(`libfoo.so.0.1`)。如果版本不匹配，这可能会导致符号错误，我们将在下一节中讨论这个问题。

当可执行文件使用共享库文件时，通过使用 [ldd](https://linux.die.net/man/1/ldd) 实用程序检查可执行文件，很容易检查它使用了哪些直接依赖项(编码在可执行文件中),该实用程序有一个问题，它不能很好地与旧的`a.out`格式一起工作。对于 Windows、Linux/BSD 和 MacOS 上的现代开发来说，这并不是一个问题，它们分别使用 PE (PE32+)、ELF 和 Mach-O 格式。对于嵌入式开发(如 ARM Cortex-M)，ELF 格式也用作生成二进制映像之前的中间格式。

## 列出依赖关系

来自`ldd`的基本输出显示了在文件系统的什么地方找到了直接依赖关系，以及哪些依赖关系没有找到。例如，这是 Windows 上 MSYS2 下`ffplay.exe`的`ldd`的(重度)缩写输出:

```
$ ldd /mingw64/bin/ffplay.exe
        ntdll.dll => /c/Windows/SYSTEM32/ntdll.dll (0x77780000)
        kernel32.dll => /c/Windows/system32/kernel32.dll (0x77660000)
        KERNELBASE.dll => /c/Windows/system32/KERNELBASE.dll (0x7fefd730000)
        msvcrt.dll => /c/Windows/system32/msvcrt.dll (0x7fefed80000)
        SHELL32.dll => /c/Windows/system32/SHELL32.dll (0x7fefdab0000)
        SHLWAPI.dll => /c/Windows/system32/SHLWAPI.dll (0x7fefda10000)
        GDI32.dll => /c/Windows/system32/GDI32.dll (0x7feff0e0000)
        USER32.dll => /c/Windows/system32/USER32.dll (0x77560000)
        LPK.dll => /c/Windows/system32/LPK.dll (0x7fefeb30000)
        USP10.dll => /c/Windows/system32/USP10.dll (0x7feff6e0000)
        SDL2.dll => /mingw64/bin/SDL2.dll (0x644c0000)
        [...]

```

显示的一般可执行文件的依赖关系可能相当庞大(完整的列表大约是这个长度的八倍)，但是作为一个快速的完整性检查，不仅可以查看依赖关系是否已经实现，还可以查看应用程序加载器是否选择了正确的库。例如，一个系统可能有两个不同版本的库(例如，在 */usr/shared/bin* 和 */usr/bin* )，这可能会导致令人捧腹的情况，您会花半天时间调试不同的库和应用程序版本，回滚“已知工作”的代码版本，并失去理智。

像`ldd`这样的工具显示的另一件事是库在哪个地址被加载，但这只对真正高级别的调试和优化有用。

## 当符号消失时

当我们在可执行文件和库格式的上下文中谈论符号时，事情变得有趣了。这不是关于调试符号，这是一个完全不同的主题，而是使代码段可能被找到的不可或缺的符号，无论是在执行时，还是在将目标文件和静态库链接在一起时。缺少符号也会导致有趣的运行时错误，在某些共享库中找不到“入口点”。

解决此类问题的一个快速方法通常是确保您拥有与代码或可执行文件相匹配的库版本。有时这些都检查过了，应用程序加载器或链接器工具仍然告诉你缺少符号，那么这是怎么回事呢？

在链接代码的情况下，它可以简单到链接顺序错误，因为大多数语言的工具链使用一种机会主义的链接风格，它记住丢失的符号，但不记得它已经看到的符号。虽然在像 Ada 这样的语言中这不是问题，但在 C 风格的语言中，确定给予链接器工具的命令中的链接顺序是至关重要的。

另一个问题是语言(如 C++)支持重载函数以支持不同的参数和返回类型，并使用名称篡改(以获得唯一的符号)。如果一个头文件是在 C++模式下编译的，当它应该被链接到一个被编译成 C 代码的库时，没有名字混淆，这将使链接器工具为那些函数给出“缺少符号”的错误。

为了弄清楚一个丢失的符号是真的丢失了，还是被不恰当地破坏了，是被弄混了，还是在另一个库或目标文件中，人们可以使用类似于 [readelf](https://linux.die.net/man/1/readelf) 的实用程序来检查文件中实际上有哪些符号。注意(显然)readelf 只支持 elf 风格的文件。一个更通用的工具是 [nm](https://linux.die.net/man/1/nm) ，它只关注各种格式的符号。例如，nm 上的[维基百科条目](https://en.wikipedia.org/wiki/Nm_(Unix))的输出:

```
# nm test.o
0000000a T _Z15global_functioni
00000025 T _Z16global_function2v
00000004 b _ZL10static_var
00000000 t _ZL15static_functionv
00000004 d _ZL15static_var_init
00000008 b _ZZ15global_functioniE16local_static_var
00000008 d _ZZ15global_functioniE21local_static_var_init
         U __gxx_personality_v0
00000000 B global_var
00000000 D global_var_init
0000003b T main
00000036 T non_mangled_function

```

这显示了使用 C++编译器时 nm 的输出。如果有必要，Nm 可以被指示去混淆符号以使其更容易阅读。不管怎样，它的输出告诉我们一个符号是存在于文件中还是未定义的(' U ')。它还将详细说明符号的定义位置(哪个部分)以及符号的类型(如果相关)。在上面的例子中，我们看到一个未定义的符号(' U ')、几个文本(代码)段符号(' T' & 't ')、一个未初始化数据段中的符号(BSS，' B' & 'b ')和两个已初始化数据段中的符号(' D' & 'd ')。

其中，我们只需要给链接器一个包含一个未定义符号的库或目标文件，就可以链接代码并生成一个可执行文件。

## 最后一招:跟踪应用程序启动

令人恼火的是，有时一切似乎都很正常，但应用程序无法启动，或者中途退出，并显示一条神秘的消息。这就是像 [strace](https://linux.die.net/man/1/strace) 这样的实用程序非常有用的地方，因为它从应用程序启动的那一刻起就跟踪涉及应用程序的所有系统调用。通常，应用程序无法加载的问题是由于无法加载的间接依赖关系、不适当的环境设置或者文件被意外设置为只读。

只需使用 application as 参数启动 strace，就会输出应用程序发出的系统调用列表，包括错误，如丢失文件:

```
open("/foo/bar", O_RDONLY) = -1 ENOENT (No such file or directory)

```

或者缺少库依赖项:

```
open("/usr/lib/libfoo.so", O_RDONLY|O_CLOEXEC) = -1 ENOENT (No such file or directory)
```

## 包扎

显然，这些都不是调试可执行文件、二进制文件和各种相关问题的链接和运行的最终目的。就像生活中的许多事情一样，最终最重要的是经验。随着时间的推移，人们会对问题所在以及如何尽快找出罪魁祸首有一种直觉。

我在商业软件开发领域工作了很多年，经历了一系列(过于)雄心勃勃的业余爱好项目，可以肯定地说，有很多知识我希望自己能早点掌握。另一方面，发现为什么有些事情行不通并纠正这种违背世界秩序的不公正的行为本身通常是有益的。

也就是说，人们必须明智地选择他们的战斗。有时候从零开始学习东西是不值得的，依靠别人的知识也没什么好羞愧的。尤其是在周五下午，客户希望新版本在周一交付。希望这篇文章在这方面有所帮助。