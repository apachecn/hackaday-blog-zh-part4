# Twist 承诺更容易的量子编程

> 原文：<https://hackaday.com/2022/02/05/twist-promises-easier-quantum-programming/>

我们一直试图了解更多关于量子计算机的知识。但事实是，我们今天对量子计算机或其模拟器编程的方式可能与我们未来对它们编程的方式没有太多共同之处。想想吧。给你的电脑编程和给 ENIAC 编程完全不同。因此，我们预计我们将看到越来越多的“裸机”量子计算机的抽象概念。其中最新的是麻省理工学院的 [Twist](https://news.mit.edu/2022/new-language-quantum-computing-twist-0124) 。

根据[论文](https://dl.acm.org/doi/10.1145/3498691)(以及下面的视频)，Twist 以传统程序员可以理解的方式表达纠缠的数据和过程。关键的概念被称为表达式的“纯度”,这有助于编译器确定数据是否实际上与另一段数据纠缠在一起，或者任何潜在的纠缠是否无关。纯表达式只依赖于它所拥有的量子位，而混合表达式可能会使用其他表达式所拥有的量子位。

这是 Twist 中一个传送程序的例子:

[![](img/b04d3462e9388c7026256012e11eed7d.png)](https://hackaday.com/wp-content/uploads/2022/02/twist_detail.png)

这看起来可能很奇怪，但是丢弃一个量子位和测量它有相同的效果，所以丢弃一个中间结果会影响一个看起来没有立即关联的纠缠结果。这与传统编程中释放两个不同指针使用的内存的方式类似。比如说，丢弃包含雇员记录的内存，同时持有指向同一记录的另一个指针，如果以后重用该内存，将会导致问题。然而，使用 Twist，你可以向编译器保证纯表达式之间没有纠缠。

当然，还有很多，所以看看报纸吧。如果你需要复习基本的量子计算原理，看看我们的系列或[看视频](https://hackaday.com/2018/07/13/quantum-computing-for-computer-scientists/)。

 [https://www.youtube.com/embed/kb38c-iW1o0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kb38c-iW1o0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

