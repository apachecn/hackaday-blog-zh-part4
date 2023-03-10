# Linux Fu:Fork()的一种奇怪用法

> 原文：<https://hackaday.com/2022/04/21/linux-fu-an-odd-use-for-fork/>

如果你是《星际迷航》的粉丝，你可能会记得这句话“[你必须了解为什么星舰](https://youtu.be/KJwFHrZbyAs?t=55)上的东西会工作。”事实是，在大多数情节中，知道如何控制另一艘船的控制台或制造火药并不是很方便，但当它做到时，它真的拯救了世界。Linux 很像那样。有一些事情你可能不需要经常知道，但是当你需要知道的时候，就会有很大的不同。在这篇文章中，我想看看`fork`系统调用的奇怪用法。出于许多目的，你永远不需要知道这种特殊的不规则使用。但是当你需要它的时候，你真的会需要它。

这实际上是基于我的一个老客户，他每天使用 Unix 运行一个大规模的非常关键的报告。该报告有大量的数学计算，因为他们试图优化一些东西，然后生成大量的报告。在那些日子里，报告的输出是在行式打印机的旧绿条纸上。问题是，包括打印输出在内，这份报告花了大约 14 个小时。如果有人发现了错误，就没有时间再次运行报告，因为第二天的报告必须在第二次运行完成之前开始。

客户有一群 Windows 程序员，而且——在那个时候——在 Windows 中没有任何类似于真正的`fork`调用的东西。我看了看代码，意识到可能大部分代码都在花费时间等待打印输出。计算机有多个 CPU 和多台打印机，但是一个程序挂在一台打印机上。有大量的数据，所以将其写入数据库，然后针对它运行不同的报告并不是一个好的选择。答案是利用`fork`的力量。不到 30 分钟就完成了代码更改，报告在 5 个小时内完成。他们非常高兴。

那么我是怎么做到的呢？答案在于`fork`如何运作。几乎每次你看到一个`fork`，你就会看到某种`exec`呼叫开始一个新的程序。因此，如果你想到`fork`，你可能会认为这是你如何开始一个新程序的一部分，大多数时候，这是真的。

## `fork()`到底是做什么的？

然而，这个调用做了一些非常奇怪的事情。它实际上将整个正在运行的进程复制到一个新的进程中。然后它运行新的进程。当然，原始进程也在运行。通常，当你看到 fork 时，它看起来像这样:

```

int childPID;
childPID = fork();
if (childPID == 0) exec....; /* load child program and run that */
/* the parent only gets here with childPID set to the new process' PID */
...

```

[![](img/b9bbf4c05a06a6873ca23cc0f47ce7d9.png)](https://hackaday.com/wp-content/uploads/2022/04/fork.png) 换句话说，`fork`的返回值对于子进程是零，对于父进程是其他值。一些早期的 Unix 系统在运行过程中真的是什么都抄。然而，这真的是低效的，尤其是当大多数时候你只是立即加载一个新的程序。

现代系统使用 COW 或 Copy On Write 语义。这意味着新进程得到的是一个指向原始进程内存的指针，当子进程或父进程对内存区域进行更改时，它只复制相对少量的内存。这对于像指令空间这样无论如何都不应该改变的东西是有好处的，因为很少有人仍然编写自修改代码。这意味着在一个`fork`调用之后，父母和孩子都看到完全相同的数据，但是他们所做的任何改变都不会反映到另一方。

## 轻松实现并行处理

对于我的客户的长篇报告来说，程序大部分是 I/O 绑定的。然而，除了到达每个报告可以执行的点所需的所有数学运算之外，每个报告也有一些非常复杂的数学运算。我没有在一个进程中执行所有的程序，而是将程序分成了多个部分。第一篇文章尽可能多地运用了数学知识，几乎适用于所有事物。然后程序调用`fork`很多次，每个孩子开始一个报告，这个报告为自己做了一点数学计算，并要求一个打印机来写输出。

由于 CPU 有多个处理器，一切都加快了速度。报告三不必等待报告一和报告二完成。每个人都能立刻开动打印机。这是一个全面的胜利，它几乎没有花时间来解决这个问题。

当然，并不是每个问题都允许像这样的修复。但是，与从文件或数据库中读取数据相比，为每个报告进程提供数据的内存副本要快得多。在报告开始后，数据没有变化，所以实际的内存消耗也不算太大。

## 一个例子

那么真的有那么简单吗？确实是。现在唯一的问题是，使用现代机器，很难找到一个简单的问题来演示这项技术。我最终决定只做一些简单的事情，但是要做很多。我虚构的任务是:用一些虚构但可预测的数据填充一个非常大的双精度浮点数数组，然后求平均值。我说的“非常大”是指 5500 万个条目或更多。

[![](img/161698dc1c0b75c7525fc706c9e648a3.png)](https://hackaday.com/wp-content/uploads/2022/04/bench.png) 我编写了一个程序，可以用两种方式完成这项工作。首先，它只是尽可能以最简单的方式做到这一点。一个循环遍历数组中的每一项，将它们相加，最后相除。在我的机器上，运行几次平均需要 458 毫秒——使用`time`命令来计算。

程序也可以在命令行上接受一个`F`参数。当它生效时，设置是相同的，但是 fork 创建了两个进程来将数组分成两半，并计算每一半的平均值。我不想让孩子与这个过程交流，但这当然是可能的。相反，你只需要读取两个平均值，将它们相加，然后除以 2，就可以得到真正的平均值。我不想增加传达结果的开销，但这很容易做到。

分叉版运行的时间？大约 395 毫秒。当然，您的结果会有所不同，虽然 60 毫秒左右似乎不是很多，但它确实表明，两个进程一起工作可以允许多个内核同时工作。

阵列越大，节省的时间就越多。例如，将大小设置为 155，256，000 显示节省了大约 150 毫秒。当然，这些时间安排并不科学，需要考虑的因素也很多，但是数据清楚地表明，在两个进程之间划分工作会更快。

## 代码

代码很简单。这项工作并不难，只是工作量很大。

```

#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>
#include <sys/wait.h>

// compile: gcc -o stress stress.c
// run: time stress
// time stress F

#define SIZE 55256000 // how big is the array?
double bigarray[SIZE];

// The process routine will go from llimit to ulimit
// For the single case, that's everything
// For the child case we will split in half
unsigned int ulimit=SIZE;
unsigned int llimit=0;

double total; // running total

// Load up the array with some bogus data
void setup(void)
   {
   unsigned int i;
   for (i=llimit;i<ulimit;i++)
      {
      bigarray[i]=i/3.0f;
      }
   }

// Average the range defined by llimit and ulimit
void process(void)
   {
   unsigned int i;
   unsigned int n=ulimit-llimit;
   total=0.0;
   for(i=llimit;i<ulimit;i++)
      {
      total+=bigarray[i];
      }
   printf("Avg=%f\n",total/n);
   }

int main(int argc, char *argv[])
   {
   int dofork=0;
   int pid;
   if (argc>1 && (*argv[1]=='f' || *argv[1]=='F')) dofork=1; // f or F will trigger a fork
   setup(); // load array
   if (!dofork)
      {
// single case
// ulimit and llimit are already set
      process();
      exit(0);
      }
   else // forking here
      {
      if (pid=fork())
         {
// parent -- adjust ulimit
         ulimit=SIZE/2;
         process();
         waitpid(pid,NULL,0); // wait for child
         exit(0);
         }
      else
         {
// child -- adjust lower and upper limit
         llimit=SIZE/2;
         ulimit=SIZE;
         process();
         exit(0);
         }
     }
// we never get here
   }

```

## 为什么星舰上的东西会工作

现在你知道了`fork`的真正工作原理。嗯，算是吧。关于哪些句柄可以传递给子进程，哪些不能，有很多细微差别。而且，正如我所说的，你不会经常需要这个。但有时它真的会拯救世界。

如果你想更深入地了解多任务处理，试试旧的 Linux 版本。或者，检查一下 [GNU 并行工具](https://hackaday.com/2020/06/29/linux-fu-parallel-universe/)。