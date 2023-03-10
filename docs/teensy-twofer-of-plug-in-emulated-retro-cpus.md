# 插件仿真复古 CPU 的 Teensy Twofer

> 原文：<https://hackaday.com/2022/12/26/teensy-twofer-of-plug-in-emulated-retro-cpus/>

[Ted Fried]写的不是一个而是两个(2！)广泛使用的老式 CPU 的新替代品:Zilog Z80 和 T2 的英特尔 8088 T3。这两种“芯片”都以周期精确模式和超级涡轮模式运行，这种模式可以运行得如此之快，以至于你需要使用 Teensy 的内部 RAM 才能跟上。

这两种设计都有硬件和软件组件。PCB 基本上是根据目标 CPU 调整 Teensy 的引脚排列，板上有一堆 74VLC 锁存器来进行电压电平转换。剩下的事情就是模仿 Teensy 上的所有指令，这比足够快的速度要快得多。如果这听起来对你来说很熟悉，这基本上就是[Ted]去年为我们带来[他在苹果[和 Commodore 64 中发现的 6502](https://hackaday.com/2021/11/03/vintage-computers-with-a-real-turbo/)的替代品所用的相同方法。

当原始 CPU 仍然可用时，您为什么想要一个仿真 CPU 呢？[Ted]继承了一个坏掉的 Osborne I，一个古老的 Z80。通过用他的仿真替换原来的 Z80，他可以诊断整个系统，这使他发现了一些坏的 DRAM 芯片，并使旧的野兽再次运行。或者也许你只是想[以疯狂的速度玩 IBM XT 游戏](https://microcorelabs.wordpress.com/2022/07/31/mcl86-8088-accelerator-update/)？

而且看起来[Ted]已经更新了他的 6502 仿真，包括了未记录的 C64 操作码，所以如果你喜欢那个场景，你也应该被覆盖。

如果这些引起了你的兴趣，去[Ted]的博客， [microcore labs](https://microcorelabs.wordpress.com/) 看看吧。尽管现在他已经介绍了大多数著名的逆向计算机，我们必须问自己下一个处理器会是什么？