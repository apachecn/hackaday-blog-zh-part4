# Linux Fu:简单管道

> 原文：<https://hackaday.com/2022/03/16/linux-fu-simple-pipes/>

在过去，你有一台电脑，它一次只做一件事。字面上。你可以装入卡片或穿孔带或其他东西，然后按下按钮。计算机会读取你的程序，执行它，然后输出结果。然后它会回到睡眠状态，直到你给它更多的输入。

问题是电脑——尤其是在当时——非常昂贵。对于一个典型的程序来说，计算机要花很多时间等待下一张穿孔卡片的出现或磁带到达正确的位置。在这种情况下，计算机象征性地用脚敲打，等待下一个事件。

一些聪明的人意识到计算机在等待的时候可能在做别的事情，所以你应该一次输入多个程序。当程序 A 在等待一些 I/O 操作时，程序 B 可以取得一些进展。当然，如果程序 A 不做任何 I/O，那么程序 B 就会挨饿，所以我们发明了抢占式多任务处理。在该方案中，程序 A 一直运行，直到它不能再运行，或者直到预设的时间限制出现，无论哪一个先出现。如果时间到了，程序被迫休眠一会儿，这样程序 B(和其他程序)就轮到它们了。除了微型嵌入式系统之外，几乎所有现代计算机都是这样工作的。

但是还是有区别的。现在大多数计算机都有多个 CPU 和快速切换任务的特殊方法。我写这篇文章的桌面有 12 个 CPU，每个 CPU 可以像两个 CPU 一样工作。因此，计算机可以同时运行多达 12 个程序，并且有另外 12 个程序可以非常迅速地替换任何一个活动的程序。当然，操作系统也可以在那 24 个程序堆上打开和关闭程序，所以你可以运行更多的程序，但是主 12 和备份 12 之间的切换非常快。

因此，使用多个程序编写解决方案的理由比以往任何时候都更加充分。有很多好处。例如，我曾经接管了一个程序，它进行了大量的计算，然后花了几个小时打印出结果。我将打印分离到不同的打印机上，减少了 80%的运行时间——这几乎是我开始工作时的一天。但是即使在性能之外，进程隔离也像是最终的封装。你在程序 A 中做的事情不应该影响程序 b，就像我们把代码隔离在模块和对象中一样，我们可以更进一步，把它们隔离在进程中。

## 双刃剑

但这也是个问题。据推测，如果你想让两个程序合作，它们需要以某种方式相互影响。你可以只用一个文件在它们之间进行交流，但这是出了名的低效。所以像 Linux 这样的操作系统提供了 IPC——进程间通信。就像你将一个对象的某些部分公开一样，你也可以将你程序中的某些东西公开给其他程序。

最基本的方法是使用`fork`调用。当您派生一个新流程时，该新流程是其父流程的完整副本。你并不总是意识到这一点，因为你经常做的下一件事是调用类似于`exec`的东西来加载一个新程序，或者你使用一个类似包装器的系统来为你调用`fork`和`exec`。但是每次你在命令提示符下运行`ls`时，你正在运行的`ls`程序就像是 shell 的一个完整副本。然后，该副本加载并运行`ls`可执行文件。

但如果没有呢？这就是我的报告作者的工作方式。在一台有很多 CPU 的连续计算机上花费几个小时的大型数学运算发生在一个进程中。到了打印的时候，我分出一堆子流程。每个人都有一份完整的数据拷贝，然后我把它当作只读文件，开始打印。这是进程间通信的一种方式。

另一种方式是管道。想象这样一个命令行:

```
cat data.txt | sort | more
```

在这里，您创建了三个流程。一种是从文本文件中转储数据。它将数据发送到连接到`sort`程序的管道。它输出到连接到`more`程序的另一个管道。

## 单程

[![](img/bcc329c37d4671b8ed91104ec6ef6579.png)](https://hackaday.com/wp-content/uploads/2022/03/1way.png) 像这样的管道是单向事务，但是您可以创建命名管道并在两个方向上讨论它们。您可以在 shell 中完成这两项工作— `mknod`创建一个命名管道—但是您也可以在程序中完成这两项工作。(`popen`对于普通管道来说非常容易使用，并且还有一个`mknod` API 调用。)

还有其他几种方法可以用于跨进程对话:

*   消息队列——一种向另一个流程异步发送消息的方式
*   信号量——一种与另一个程序共享计数器的方式
*   共享内存–共享一块内存
*   信号——您可以向其他进程发送信号，作为一种通信形式

你可能想知道为什么你需要共享内存以外的东西。老实说，你不知道，但在许多情况下，使用不同的方法会更容易。问题是你需要某种方式来实现原子操作，而信号量之类的东西可以帮你管理。想象一下，如果我们在共享内存中有一个名为`busy`的变量。如果`busy`是 1，那么我们知道我们不应该改变共享内存中的数据，因为有人正在使用它。

我们可能会写:

```
while (busy) ; // wait for busy==0
busy=1;
do_stuff();
busy=0;
```

看起来很棒，对吧？不。在 CPU 的某个地方，while 循环看起来像这样:

```
while_loop2384: TST busy ; set flags on busy
                JNZ while_loop2384 ; if no zero flag, jump
                MOV busy,#1 ; move 1 to busy
```

大多数情况下，这将工作得很好。大多数时候。但是，如果我执行了`TST`指令，然后我进入睡眠状态，这样另一个程序就可以运行相同的代码，会发生什么呢？或者另一个 CPU 在完全相同的时间运行完全相同的代码？这是有可能发生的。所以两个程序现在都会看到`busy`是零。然后他们都会把`busy`设为 1，继续下去。那是失败的。

信号量通过原子访问机制来管理这一点，该机制允许程序在一个地方测试和设置操作。还有更多要担心的，比如如果我在等待进程 B 释放一个信号量，而进程 B 在等待我释放另一个信号量，会发生什么。但是这种情况——死锁——是将来的话题，还有其他隐藏的问题，比如优先级反转。

## 在准备中

[![](img/588ea7acf23f278dde41f346b5c8f64d.png)](https://hackaday.com/wp-content/uploads/2022/03/pipe-3.png) 我有一点编出来的问题。在 Linux 上，如果我输入`df`就可以找到所有挂载的东西及其特征。但是该列表包括诸如根目录和交换文件之类的东西。如果您只想读取环路设备并显示相同格式的输出，会怎么样？当然，有很多方法可以做到这一点。您可以从/etc/mtab 中读取循环文件，然后从/sys 或它所在的任何地方读取其他数据。听起来工作量很大。

当然，跑`df`会让我们快到那里。事实上，我可以在 shell 中运行一个管道来得到我想要的东西，类似于:

```
df | grep '^/dev/loop'
```

这是可行的，但输出是混乱的。在我的系统上，第一个是/dev/loop3，最后一个是/dev/loop0，没有明确的理由说明为什么数字 4 在 8 和 14 之间。所以想整理一下。通过管道排序没有太大帮助，因为它将按字母顺序排序。您可能会考虑给`sort`加-n 标志，但这不会起作用，因为数字在字符串的末尾。当然，我可以使用一些奇怪的组合`cut`或`sed`来修复这一切，但是这变得太复杂了。我们就写 C 代码吧。

第一步是让`df`打印所有内容并捕获输出。因为我们想要处理输出，所以我们需要读取一个管道，而`popen()`是设置这个管道的一个简单方法:

```

#include <stdio.h>
int main(int argc, char * argv[]) {
// This part reads the output of DF into the lines array (with some modifications)
   FILE * result = popen("df", "r"), * sort;
   int i;
   if (!result) {
      perror("Can't open df");
      return 1;
   }
   while (!feof(result)) {
     int c = getc(result);
     if (c != EOF) putchar(c);
   }
 pclose(result);
 return 0;
}

```

## 一半解决了

问题解决了一半。如果你有字符，你可以做所有你想要的排序和过滤，但是…等一下！我还是很懒。因此，让我们请壳牌公司来帮助我们。这是我的计划。我知道我只想要以/dev/loop 开头的行，所以让我们这样做:

*   一次读一整行
*   如果它不是/dev/loop 行，就抛出它
*   如果它是一个/dev/loop 行，那么把它保存在一个数组中，但是去掉/dev/loop 部分
*   在我们得到所有的行之后，请求 shell 进行排序，然后在排序之后将/dev/循环添加回去

很简单:

```

#include <stdio.h>
#include <string.h>

char buffer[4097];
char * lines[512];
unsigned int maxline = 0;

int main(int argc, char * argv[]) {
// This part reads the output of DF into the lines array (with some modifications)
   FILE * result = popen("df", "r"), * sort;
   int i;
   if (!result) {
      perror("Can't open df");
   return 1;
   }
   while (!feof(result)) {
 // get a line from df
     char * rc = fgets(buffer, sizeof(buffer), result);
// only save lines that start with /dev/loop
    if (rc &amp;amp;&amp;amp; !strncmp(buffer, "/dev/loop", 9)) {
// out of space
       if (maxline >= sizeof(lines) / sizeof(char * )) {
       fprintf(stderr, "Too many loops\n");
       return 2;
     }
   lines[maxline++] = strdup(buffer + 9); // copy just the number part and the rest of the line
   // should check lines[maxline[1] for null here
   }
 }
 pclose(result);

// Now we are going to print through sort
// The sed replaces the /dev/loop at the front of the line after sorting
 sort = popen("sort -n | sed 's/^/\\/dev\\/loop/'", "w");
 if (!sort) {
   perror("Can't open sort");
   return 3;
  }
// for each line, send to pipe (note order didn't really matter here ;-)
 for (i = 0; i < maxline; i++)
   fputs(lines[i], sort);
 pclose(sort);
 return 0;
}

```

现在你知道了。是的，你可以单独用 shell 来做这件事，但是这会困难得多，除非你求助于另一种编程语言，比如 awk，那样你就真的不仅仅是在用 shell 了。此外，这是一个很好的例子，你可以像这样做很多事情，否则很难做到。

您可能想知道是否可以剥离像`sort`这样的东西，既给它输入又读取它的输出。答案是肯定的，但不是用`popen()`。`popen()`调用只是`pipe`和`fork`的一个方便的包装。如果你想两端都做，你必须直接使用`pipe()`调用(两次),然后执行`sort`或其他什么。但那是未来的话题。

进程间通信还有许多其他的未来主题。但是现在，使用`popen`来尝试管道。[临界区](https://hackaday.com/2020/08/18/linux-fu-one-at-a-time-please-critical-sections-in-bash-scripts/)也在 shell 脚本中出现。如果你喜欢用 C 语言编写你的[脚本，那也是可能的。](https://hackaday.com/2019/09/17/linux-fu-shell-scripts-in-c-c-and-others/)