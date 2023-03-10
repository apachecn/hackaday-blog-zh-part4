# 斯科特的 CPU 自下而上

> 原文：<https://hackaday.com/2022/05/19/scotts-cpu-from-the-bottom-up/>

它并不适合每个人，但是如果你经常在低级别的计算机上工作，你可能迟早会有创造自己的 CPU 的想法。曾几何时，这是一个巨大的事业，但有了今天的工具和 FPGAs，这是…嗯，不容易，但肯定更容易。如果你有尝试自己的冲动，你可以看看[简单解释的]视频系列，名为“[构建斯科特的 CPU。](https://www.youtube.com/playlist?list=PLnAxReCloSeTJc8ZGogzjtCtXl_eE6yzA)

这 11 个视频涵盖了从基本晶体管逻辑到时序电路的所有内容，并转移到 alu、时钟单元和跳转指令如何工作等方面。

我们猜测会有更多的视频出现。然而，这 11 个视频的内容超过了两个小时，这对您来说是一个很大的开始。当然，每个从事这项工作的人通常必然会专注于一种类型的架构，但是有许多方法可以用来设计 CPU。许多自制设计是简单的多时钟指令设计。一些使用流水线技术，一旦流水线填满，每个时钟获得一条指令。平均来说，现代的 CPU 在每个时钟周期执行很多指令，但是这使得很多事情变得复杂了。

此外还有非传统架构，如单指令计算机或异步 CPU。关键是，一旦你知道一个基本的 CPU 是如何工作的，在你自己的设计中仍然有足够的空间去创新。

我们已经不止一次地经历过这个练习，在我们看来，最困难的部分不是创建 CPU。这是[建立所有的辅助工具](https://hackaday.com/2015/07/31/build-your-own-cpu-thats-the-easy-part/)你需要做任何有用的事情。有一些[的技巧让这变得更容易](https://hackaday.com/2015/08/06/hacking-a-universal-assembler/)。另一方面，从 A 到 Z 的所有事情都可以做[。](https://hackaday.com/2017/01/13/fpga-computer-covers-a-to-z/)

 [https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLnAxReCloSeTJc8ZGogzjtCtXl_eE6yzA](https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLnAxReCloSeTJc8ZGogzjtCtXl_eE6yzA)

