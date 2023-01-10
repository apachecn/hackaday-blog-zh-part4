# 使用 Valgrind 追踪代码中已知和未知的 bug

> 原文：<https://hackaday.com/2020/04/29/using-valgrind-to-track-down-known-and-unknown-bugs-in-your-code/>

我们都知道代码中的 bug 是什么。我们不喜欢它们出现在我们使用的程序中，更不喜欢它们出现在我们编写的代码中。很明显，最好的代码是没有错误的，但是我们如何实现呢？

当然，这不是一个新问题，只是随着现代社会运行的代码行(LoC)总数不断增加，这个问题变得越来越重要，而且现在每个东西都有一个微控制器，这甚至越来越多地影响到业余爱好者。

尽管我们中的许多人都知道在为一个项目运行单元测试之后，看到一整行绿色的结果标记全面亮起时的那种自鸣得意的满足感，但是痛苦的现实是，直到代码在类似于生产环境的环境中运行时，您才知道它是否真的在功能上是正确的。然而，在这种情况下，如何测试应用程序呢？

这就是 Valgrind 套件中包含的工具发挥作用的地方，它允许我们分析、剖析和挑剔每一个操作码和内存读写。我们来看看，好吗？

## 它坏了，让它重新工作

当谈到软件开发(在某种程度上也包括硬件开发)时，有三种可能被打破的状态:

1.  很明显坏了。
2.  它能工作，但有时会坏掉。
3.  它工作正常，但实际上已经坏了。

第一种类型不会让任何人感到惊讶。这种故障会令人愉快地用诸如' [SIGSEGV](https://en.wikipedia.org/wiki/Segmentation_fault) '(分段故障)和' [SIGBUS](https://en.wikipedia.org/wiki/Bus_error) '(地址总线故障)这样令人愉快的术语来宣布自己，这表明操作系统的内核已经检测到应用程序将要做一些非法或不可能的事情。[除以零](https://en.wikipedia.org/wiki/Division_by_zero)就是后者的一个很好的例子。

第二种类型的中断——确实运行，但有时会抛出错误——更有趣，因为它允许应用程序正常运行，传输数据，打开和写入文件，以及在屏幕上显示数据，而不会出现任何问题。直到第二次做同样的事情时，突然失败了。或者在一个小时的正常工作后，它失败了。或者它开始做一些“奇怪”的事情，之后应用程序的行为开始感觉几乎是随机的。

第三种类型的破碎——在它运行但它不应该运行的地方——也被称为“这究竟是如何在第一时间起作用的”,它的发现通常伴随着大声的惊呼，对现实结构的质疑，以及可能对一个人选择的神的一些快速祈祷，这取决于神学的亲和力。这种代码已经设法在一场完美的错误风暴中达到了完美的平衡，这使得它完全有机会做正确的事情。当然，直到有人敢于修改一行代码。

## 这不是魔法，只是很复杂

最基本的形式，软件仅仅是底层硬件的一系列指令。该硬件试图尽最大能力执行这些指令，这不仅涉及 CPU 的处理核心，还涉及其高速缓存、高速缓存同步逻辑(对于多核 CPU)、内存控制器和系统内存。在此之上，通常有一个操作系统(OS ),它使应用程序开发人员的生活变得轻松，因为他们不必担心实现任务调度器、堆和堆栈管理，以及许多其他有趣的细节，没有应用程序开发人员想弄乱它们。

操作系统和底层硬件的每个元素都会影响代码的执行，每个问题都会影响整个系统的不同部分。这就是为什么我们需要一系列的工具。在 Valgrind 这样的套件中，我们发现自己使用的主要工具被称为 *Memcheck* 、 *DRD* 和 *Helgrind* 。

## 使用 Valgrind 监控内存

Valgrind 启动时使用的默认工具是 [Memcheck](https://www.valgrind.org/docs/manual/mc-manual.html) 。顾名思义，它检查内存。更具体地说，它在操作系统和被测试的应用程序之间插入了一个层。就像调试器一样，它跟踪每次内存读写，跟踪引用、有效内存范围、内存块是否仍然可达等等。

Memcheck 的常见用例是检测内存泄漏，例如:

```

void main() {
	int* foo = new int;
	int* bar = new int;
	*foo = 42;
	*bar = 24;
	bar = foo;
}

```

它会在 Memcheck 日志中显示类似这样的内容:

```
4 bytes in 1 blocks are definitely lost in loss record 1 of 14

```

随后是指示何时丢失对数据(先前由`bar`指向)的访问的回溯。当将`*--leak-check=full*`传递给 Memcheck 时，它还会让您知道已经丢失的数据被分配到了哪里。这里 Memcheck 可能会报告“肯定的”、“间接的”或“可能的”数据丢失。除非有明显的问题，否则“肯定”丢失的数据块才是需要关注的。间接丢失的数据通常是由于丢失了一个指针块的地址，因此解决“明确丢失”的问题也可以解决任何“间接丢失”的问题。

通常，人们可以使用以下 CLI 命令运行 Memcheck 来获取最有用的信息:

```
$ valgrind --tool=memcheck --log-file=memcheck00.txt --leak-check=full --read-var-info=yes path/to/binary

```

这样，输出将被写入日志文件(memcheck00.txt ),我们将获得完整的泄漏报告，memcheck 将使用二进制文件中的任何调试信息(如果存在的话),以使跟踪更具可读性。强烈建议使用具有所有调试符号的二进制文件，以使人们的生活更轻松。

### 查找其他内存问题

![](img/14d80fe0821e9de7278c23b0a74fdecc.png)

Memcheck 对于检测无效的读写以及释放应用程序没有分配的内存也非常有用。这将表明应用程序正在对内存做一些淘气的事情，这可能会导致崩溃，损坏数据和其他乐趣。这还包括使用不匹配的`free()`和`delete()`调用，当在同一个应用程序中混合 C 和 C++代码时，这可能是一个问题。

最后，Memcheck 还将检查您对 malloc 和类似的内存分配函数的参数，以及 memcpy 和类似的 C 函数的参数，如果幸运的话，可以捕捉到许多在测试过程中可能会出现的问题。 [Memcheck 手册](https://www.valgrind.org/docs/manual/mc-manual.html)有各种各样的例子，各种 Memcheck 教程[也有](https://web.stanford.edu/class/cs107/resources/valgrind)(比如[这本](https://eklitzke.org/an-introduction-to-valgrind-memcheck)，它涵盖了调试内存泄漏)。

## 把你的线放在我们能看到的地方

Valgrind 中另外两个非常有用的工具是 [Helgrind](https://valgrind.org/docs/manual/hg-manual.html) 和 [DRD](https://valgrind.org/docs/manual/drd-manual.html) ，它们主要关注多线程以及由此可能导致的所有问题。根据所使用的设置，它们可以以相当粗略的方式跟踪线程活动，或者记录每个互斥体的移动等等。当然，跟踪得越多，应用程序就越慢。

虽然让瓦格兰拥有两个乍一看似乎能做同样事情的工具似乎有些多余，但赫尔格兰和 DRD 并不完全相同。每一种都使用不同的方法来分析应用程序行为，因此每一种都可能给出(稍微)不同的结果。出于这个原因，同时运行两者通常是个好主意。

我们可以使用 Helgrind 和 DRD 追踪到的问题是死锁，两个或多个线程试图获得一个资源的锁(互斥锁、rwlock 或类似的锁),同时它们自己也持有一个锁。因为每个线程只有在获得另一个锁之后才会释放它们的锁，所以什么都不会发生，应用程序实际上被冻结了。

使用 DRD，我们还可以跟踪锁的行为，包括特定锁被持有的时间:

```
$ valgrind --tool=drd --exclusive-threshold=10 drd/tests/hold_lock -i 500
...
==10668== Acquired at:
==10668==    at 0x4C267C8: pthread_mutex_lock (drd_pthread_intercepts.c:395)
==10668==    by 0x400D92: main (hold_lock.c:51)
==10668== Lock on mutex 0x7fefffd50 was held during 503 ms (threshold: 10 ms).
==10668==    at 0x4C26ADA: pthread_mutex_unlock (drd_pthread_intercepts.c:441)
==10668==    by 0x400DB5: main (hold_lock.c:55)

```

这里我们设置了一个 10 毫秒的阈值，测试应用程序被指示持有锁 500 毫秒。正如我们所看到的，根据 DRD 的说法，锁(互斥体)持有了 503 毫秒。

### 有时候秩序很重要

Helgrind 的一个有用特性是跟踪锁的正常使用顺序，以及它们的顺序何时改变:

```
Thread #1: lock order "0x7FF0006D0 before 0x7FF0006A0" violated

Observed (incorrect) order is: acquisition of lock at 0x7FF0006A0
   at 0x4C2BC62: pthread_mutex_lock (hg_intercepts.c:494)
   by 0x400825: main (tc13_laog1.c:23)

 followed by a later acquisition of lock at 0x7FF0006D0
   at 0x4C2BC62: pthread_mutex_lock (hg_intercepts.c:494)
   by 0x400853: main (tc13_laog1.c:24)

Required order was established by acquisition of lock at 0x7FF0006D0
   at 0x4C2BC62: pthread_mutex_lock (hg_intercepts.c:494)
   by 0x40076D: main (tc13_laog1.c:17)

 followed by a later acquisition of lock at 0x7FF0006A0
   at 0x4C2BC62: pthread_mutex_lock (hg_intercepts.c:494)
   by 0x40079B: main (tc13_laog1.c:18)

```

锁的使用方式是，在应用程序的整个执行过程中，以不同的顺序使用锁可能是完全有效的，也可能表示存在逻辑错误。

### 关于多线程流的思考

这两个工具都将跟踪数据竞争，当两个或多个线程试图同时访问同一资源时，会发生数据竞争，而没有锁定机制或使用原子来防止数据损坏或更糟的情况。这可能就像一个无符号 64 位整数被一个线程读取而另一个线程写入一样微妙。如果读取操作不是原子的(即，在一个 CPU 周期中读取整个 64 位值)，则该值可以在读取操作中途被写入线程改变。

数据竞争通常是坏消息，必须解决。尽管即使对于原子操作(例如，在大多数架构上读取一个布尔值或 8 位整数)也会报告数据竞争，但是将类型指定为原子类型(例如，在 C++的 STL 的`<atomic>`头文件中)是一种让 DRD 和赫尔格兰满意的简单方法，同时也是编写多线程代码的技术上正确的方法。

## 但是等等，还有更多

在本文中，我们只讨论了对调试最有用的 Valgrind 工具，因为这些往往是内存和多线程相关的问题。这为任何软件开发人员提出了另一个非常有趣且有教育意义的追求:优化代码。

在您的应用程序停止崩溃、不再破坏数据并正常运行之后，还有什么比深入研究其性能统计数据以发现更多性能更好的时间利用方式呢？这就是 Cachegrind、Callgrind 和 Massif 等工具有助于找出应用程序中的瓶颈所在，以及应该集中精力进行优化的地方。

然而，我们将不得不把这个快乐的话题留到下一天。