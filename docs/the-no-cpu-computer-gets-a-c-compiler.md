# 无 CPU 计算机得到一个 C 编译器

> 原文：<https://hackaday.com/2019/04/26/the-no-cpu-computer-gets-a-c-compiler/>

c 是最完美的语言，它可以在任何东西上运行。它甚至可以在没有 CPU 的电脑上运行。

这里所说的电脑是 giga tron T1，这是一台全功能的“家用电脑”,类似于 70 年代末和 80 年代初的那种，配有 VGA 输出。Gigatron 的特别之处在于它没有微处理器；一切都只是一个 RAM，一个 ROM，和一堆逻辑芯片。没有 ALU 芯片。或者说，有；只是整个 RISC CPU 是在基本逻辑芯片和 ROM 上的大量微码中实现的。是的，这很奇怪，但是很酷。[在](https://hackaday.com/2019/03/25/how-the-gigatron-ttl-microcomputer-works/)之前，我们已经看过了 Gigatron，通过这台计算机，你可以一瞥如果在 70 年代末有大容量存储器，工程师们会有多聪明。

虽然 Gigatron 可以用 BASIC 编程，但这种计算机的限制因素是它仍然非常难以编程。这是 8 位的家伙说的话，尽管你可以写一些简单的程序，但与 Apple II 或 C64 相比，这算不了什么。要是有一个合适的 IDE 就好了，事实上要是有一个 C 编译器就好了。这就是[pgavlin]的用武之地。他让 LCC 编译器在 Gigatron 上工作。这在技术上是一个 C 编译器，用于没有 CPU 的计算机，或者完全是 CPU 的计算机。不管你怎么看，这都令人印象深刻。

就例子和演示而言，[pgavlin]有一个康威的生命游戏工作的演示，以及一个将点放在屏幕上的程序。不多，也很慢，但是看看下面的视频。

这不是一个完整的 C 实现，因为乘法、除法、mod 和任意的左移或右移还没有被编写。浮点支持可能永远也不会完成，这并不可耻。由于内存映射碎片化的事实，硬件是有限的，但这可以通过将 Gigatron 升级到 64k 内存模型来改善。

 [https://www.youtube.com/embed/avnhPTUZ5E8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/avnhPTUZ5E8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

