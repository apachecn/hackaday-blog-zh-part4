# 分叉和运行:多重处理入门的权威指南

> 原文：<https://hackaday.com/2022/09/15/fork-and-run-the-definitive-guide-to-getting-started-with-multiprocessing/>

自 21 世纪初以来，CPU 行业已经从原始时钟速度转向核心数量。众所周知，帕特·基尔辛格在 2002 年上台发表了行业所需的演讲，称处理器需要特种硅或多核来降低功耗和散热。几年后，Core 系列推出了双核或四核配置，以与 AMD Athlon 64 x2 竞争。

如今，我们看到的异构芯片设计有大有小的内核、小芯片和其他疯狂的制造技术，它们基本上是同一个概念:将热负荷分散到多个硅片上。这位作者愿意投入大量资金打赌，在不到五年的时间里，你会看到拥有 32 个物理内核的消费台式机。可能很难相信，2013 年的英特尔 Haswell i7 只有四个内核，而今天的 i7 有 20 个内核。即使是 ESP32 也有两个内核，FreeRTOS 支持将任务锁定到不同的内核。有这么多内核，如何编写软件呢？进程和线程有什么区别？这一切在普通 C98 中是如何工作的？

## 多线程理论

进程、线程和轻量级线程是最常见的多处理类型。进程有自己的内存空间和执行上下文，必须通过 IPC(进程间调用)、管道、套接字、FIFO 文件或显式共享内存进行协调。线程是不同的执行上下文，它们组成一个进程，但共享相同的内存空间。因此，必须非常小心地确保锁定和解锁不同的状态片段，以保持数据完整性并确保正确的行为。

轻量级线程是用户空间线程。对于大多数操作系统来说，线程和进程是由操作系统管理的结构，上下文切换由内核处理。这增加了开销。一些语言在用户空间的程序内部实现线程。这种轻质线通常被称为绿色线或纤维。

## 香草派 C98

因为进程和线程是由操作系统控制的，所以 Windows 和 Unix 有不同的方法来创建和管理它们。在这一节中，我们将关注 Unix/POSIX 的方式。

对于流程来说，有一个单一的函数来完成所有繁重的工作:`fork`。

调用`fork`将返回两个值，每个进程一个。孩子将得到零分，父母将得到新孩子的新 pid。出错时，将返回一个负数。家长可以调用`waitpid`等待孩子的执行完成，得到状态。

```
#include <unistd.h>
#include <sys/types.h> 
#include <sys/wait.h>
#include <stdlib.h>
#include <stdio.h>

int main(int argc, char**argv) {
  pid_t child = fork();
  if (child == -1) return EXIT_FAILURE;
  if (child) { /* I have a child! */
    int status;
    waitpid(child , &status ,0);
    return EXIT_SUCCESS;

  } else { /* I am the child */
    // Other versions of exec pass in arguments as arrays
    // Remember first arg is the program name
    // Last arg must be a char pointer to NULL

    execl("/bin/ls", "ls","-alh", (char *) NULL);

    // If we get to this line, something went wrong!
    perror("exec failed!");
  }
}

```

孩子从父母在的地方捡起来。虽然它们不共享内存地址空间，但 Unix 会在写入时进行复制。所以他们分享，直到其中一个人改变了一些东西，然后他们得到自己的副本。当然，这种透明拷贝会导致一些奇怪的问题:

```
#include <unistd.h> /*fork declared here*/
#include <stdio.h> /* printf declared here*/
int main() {
   int answer = 21 << 1;
   printf("Answer: %d", answer);
   fork();
   return 0;
}

```

运行这个，你会看到 42 两次。`print`在`fork`之前，所以只执行一次。但是缓冲区还没有被刷新到`stdout`，所以当两个进程都退出时，它们会刷新包含“答案:42”的缓冲区。

线程有点不同。我们不使用 fork，而是使用 POSIX 线程(或者孩子们称之为`pthreads`)。`Pthread.h`是一个提供创建和管理线程功能的库。这是一个有漏洞的抽象，因为许多方面显示了 POSIX 兼容内核在幕后做什么的细节。线程通常专注于运行单个函数，而不是在特定的点分叉进程。所以代码看起来会像这样:

```
#include <pthread.h> /*pthread declared here*/
#include <stdio.h> /* printf declared here*/
void *threadedFunction(void* varp) {
   int answer = 21 << 1;
   printf("Answer: %d\n", answer);
   return NULL;
}
int main() {
   pthread_t thread_id;
   printf("Before Thread\n");
   pthread_create(&thread_id, NULL, threadedFunction, NULL);
   pthread_join(thread_id, NULL);
   printf("After Thread\n");
   return 0;
}

```

您将看到的输出是:

```
Before Thread
Answer: 42
After Thread

```

我们得到的不是进程 id，而是用于跟踪各种线程的线程 id。`join`类似于上面的`waitpid`示例，因为父线程然后等待另一个线程的终止或完成。

如前所述，线程在同一个内存空间，事情会变得很奇怪。函数内部的静态变量和全局状态都是共享的，并且是并发访问的。对于较大的结构，您可以在一个线程中将其读入内存，而另一个线程正在写入。那么您将得到一半的新值和一半的旧值，从而导致奇怪且难以调试的行为。这类问题有许多解决方案，都有不同的权衡，但它们的核心都是互斥。

让我们从一个简单的五线程彩色打印例子开始，Faye Williams 在她的博客上展示了一个简单的互斥锁。

```
#include <iostream>
#include "pthread.h"
#include <string>

using namespace std;

#define NUM_THREADS 5

#define BLACK   "\033[0m"
#define RED     "\033[1;31m"
#define GREEN   "\033[1;32m"
#define YELLOW  "\033[1;33m"
#define BLUE    "\033[1;34m"
#define CYAN    "\033[1;36m"

void* PrintAsciiText(void *id) {
    char* colour;

    switch((long)id) {
    case 0:
        colour = RED;
        break;
    case 1:
        colour = GREEN;
        break;
    case 2:
        colour = YELLOW;
        break;
    case 3:
        colour = BLUE;
        break;
    case 4:
        colour = CYAN;
        break;
    default:
        colour = BLACK;
        break;
   }

   printf("%s", colour);
   print("I'm a new thread, I'm number");
   print("%ld", (long)id);
   print("%s\n", BLACK); 
   pthread_exit(NULL);
}

int main() {
    pthread_t threads[NUM_THREADS];

    for (long int i = 0 ; i < NUM_THREADS ; ++i) {
        int t = pthread_create(&threads[i], NULL, PrintAsciiText, (void*)i);

        if (t != 0) {
            printf("Error in thread creation: %d\n" t);
        }
    }

    for(int i = 0 ; i < NUM_THREADS; ++i) {
        void* status;
        int t = pthread_join(threads[i], &status);
        if (t != 0) {
            printf*=("Error in thread join: \n", t);
        }
    }

    return 0;
}

```

乍一看，这段代码似乎很好。然而，当我们运行它时，我们得到一些令人困惑的输出。

```
I'm a new thread, I'm number I'm a new thread, I'm number, I'm a new thread, I'm number, I'm a new thread, I'm number 3
2
I'm a new thread, I'm number 4
1
0

```

当然，排序在很大程度上取决于您的操作系统和当前的处理器条件，因为这完全取决于调度程序。这些线程由操作系统管理，调度程序将按照自己喜欢的顺序运行它们。这就是互斥的用武之地。

```
#include <iostream>
#include "pthread.h"
#include <string>

using namespace std;

#define NUM_THREADS 5

#define BLACK   "\033[0m"
#define RED     "\033[1;31m"
#define GREEN   "\033[1;32m"
#define YELLOW  "\033[1;33m"
#define BLUE    "\033[1;34m"
#define CYAN    "\033[1;36m"

static pthread_mutex_t mutex;

void* PrintAsciiText(void *id) {
    string colour;
    pthread_mutex_lock(&mutex);
    switch((long)id) {
    case 0:
        colour = RED;
        break;
    case 1:
        colour = GREEN;
        break;
    case 2:
        colour = YELLOW;
        break;
    case 3:
        colour = BLUE;
        break;
    case 4:
        colour = CYAN;
        break;
    default:
        colour = BLACK;
        break;
    }

   printf("%s", colour);
   print("I'm a new thread, I'm number");
   print("%ld", (long)id);
   print("%s\n", BLACK); 
   pthread_mutex_unlock(&mutex);

   pthread_exit(NULL);
}

int main() {
    pthread_t threads[NUM_THREADS];

    for (long int i = 0 ; i < NUM_THREADS ; ++i) {
        int t = pthread_create(&threads[i], NULL, PrintAsciiText, (void*)i);

        if (t != 0) {
            printf("Error in thread creation: %d\n" t);
        }
    }

    for(int i = 0 ; i < NUM_THREADS; ++i) {
        void* status;
        int t = pthread_join(threads[i], &status);
        if (t != 0) {
            printf*=("Error in thread join: \n", t);
        }
    }

    return 0;
}

```

通过锁定和解锁互斥体，我们可以确保函数的关键部分在下一个开始之前运行完成。排序仍然是半随机的，因为作为程序开发人员，调度程序将在没有太多控制的情况下调度线程。

如前所述，存在其他解决方案，如[条件变量](https://linux.die.net/man/3/pthread_cond_wait)或[障碍](https://man7.org/linux/man-pages/man3/pthread_barrier_wait.3p.html)。希望您开始看到如何将您的程序分成不同的工作人员。如果你对更侧重于 C++的方法感兴趣，Rud Merriam [已经涵盖了你。C++用`std::thread`和`async/await`关键字在语言中构建了更多的线程，这些关键字抽象了很多线程。](https://hackaday.com/2016/07/15/code-craft-embedding-c-multitasking/)

## OpenMP

[OpenMP 是一个开源库](https://www.openmp.org/),可以放入 C 或 C++项目中，试图在多线程环境中以最小的麻烦更容易地做正确的事情。我们的目标不是将程序分成不同的线程，而是将工作负载分成不同的部分。让我们看看这个计算圆周率的程序。

```
static long num_steps = 100000;
double step;
int main () { 
  int i;
  double x;
  double pi;
  double sum = 0.0;
  step = 1.0/(double) num_steps;
  for (i=0;i< num_steps; i++) {
    x = (i+0.5)*step;
    sum = sum + 4.0/(1.0+x*x);
  }
  pi = step * sum;
}

```

OpenMP 包括许多方便的宏和函数，不管你的目标是什么操作系统，它们都能做正确的事情。它还管理线程池的创建和加入。一旦你拉进 OpenMP 头，我们简单的圆周率计算程序就会改变(但不会太大):

```
#include <omp.h> 
static long num_steps = 100000; 
double step;
#define NUM_THREADS 2 
void main () {
  int i;
  int nthreads;
  double pi;
  double sum[NUM_THREADS]; // make this an array to prevent race conditions
  step = 1.0/(double) num_steps;
  omp_set_num_threads(NUM_THREADS); 
 #pragma omp parallel 
 { 
    int i;
    int id;
    int nthrds;
    double x;
    id = omp_get_thread_num(); 
    nthrds = omp_get_num_threads(); 
    if (id == 0) nthreads = nthrds; // only one thread should copy the number of threads to the global
    for (i=id, sum[id]=0.0;i< num_steps; i=i+nthrds) { // each thread only calculates every nth part of the sum
       x = (i+0.5)*step;
       sum[id] += 4.0/(1.0+x*x);
    }
}
  for(i=0, pi=0.0;i<nthreads;i++) pi += sum[i] * step;
}

```

我们指定了`omp parallel`标签，它为我们创建了线程池，但是我们仍然需要跟踪我们的块大小和线程数量。当然，即使有一个方便的库，仍然有各种各样的技巧和优化。例如，您可以填充 sum 数组，以便每个数据块都在自己的缓存行上，不需要在核心缓存之间同步。

```
double sum[NUM_THREADS][8]; // pad of 8 assuming a 64 byte L1 cache line
// ....
sum[id][0] += 4.0/(1.0+x*x);

```

或者，OpenMP 有一个更简洁的语法，为我们处理这些细节。

```
#include <omp.h> 
static long num_steps = 100000; 
double step;
void main () {
  int i;
  double pi;
  step = 1.0/(double) num_steps;
 #pragma omp parallel private(lsum, x) shared(step)
 { 
    double lsum;
    double x;
    #pramga omp parallel for 
    for (i=0; i< num_steps; i++) { // each thread only calculates every nth part of the sum
       x = (i+0.5)*step;
       lsum += 4.0/(1.0+x*x);
    }
// Mark the next section as critical so only one thread runs at a time
    #pragma omp critical
    { pi += lsum * step; }
}
}

```

我们不需要指定线程的数量，因为框架很可能会为我们选择一个合适的数量——例如，可用内核的数量。OpenMP 非常强大，还有更多我们无法在此介绍的内容。诸如削减、时间安排、障碍和条件之类的事情。在幕后，OpenMP 仍然使用操作系统线程。其他语言提供用户空间线程来提高速度。

## 绿色线/纤维

这就很好地把我们带到了下一个话题。为了简洁起见，我们在这里不会给出任何例子，但是 [Golang(或 Go)是一种语言](https://go.dev/),它主要是出于对 C++的厌恶而发展而来的。它以“goroutines”的形式内置了线程。这些 goroutines 跨一定数量的 OS 线程进行调度，并且是轻量级或绿色线程。但是它们是由 go 运行时管理的，而不是操作系统。这是为了避免在从用户级权限转换到内核级权限时付出代价高昂的上下文切换成本。

操作系统线程需要在多个内核上运行。这被称为 M:N 调度器，因为它调度 M 个 OS 线程来运行 N 个 Go 纤程。它也不是没有缺点。先发制人的权利有限，公平性也无法保证。在 Morsing 的博客上有一篇关于 Go 中调度程序的很好的文章，并且有很有帮助的彩色图表。其他有纤程的语言包括 CPython、D、Erlang、Haskell、Julia、Lua 和 Tcl。如果您的首选语言没有实现它，那么有几十个不同语言的库提供类似的东西。

## 结论

现在，您的计算机上有了所有这些内核，您就知道如何让它们为您工作了。这里有太多的东西需要学习，比如基于事件的循环编程、[自旋锁与互斥](https://hackaday.com/2019/03/24/grabbing-the-thread-spinlocks-vs-mutexes/)、处理器如何相互通信、操作系统调度程序、[系统调用](https://hackaday.com/2016/11/19/under-the-linux-hood/)等等。希望你能拿走这里的东西，开始分叉，带着它跑。

横幅图片:Muhammad Taslim Razin 的“[勺子&叉子](https://www.flickr.com/photos/48530295@N04/5457752825)”。托尼·鲍登的《[沃维福克](https://www.flickr.com/photos/52942259@N00/3462546680)