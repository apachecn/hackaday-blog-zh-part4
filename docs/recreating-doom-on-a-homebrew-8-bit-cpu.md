# 在自制的 8 位 CPU 上重现厄运

> 原文：<https://hackaday.com/2022/08/16/recreating-doom-on-a-homebrew-8-bit-cpu/>

[詹姆斯·沙曼]一直在研究他自己设计的 8 位 CPU。自然地，随着他的计算设备功能的增强，一个显而易见的问题被提了出来:它能运行毁灭吗？[詹姆斯的]最新视频探索了这个问题，[展示了他能有多接近。](https://www.youtube.com/watch?v=OI6Q1r1TxuA)

[James'] 8 位流水线 CPU 也有自己的 UART、VGA 适配器和声音适配器，它们都构建在各种 PCB 上的分立元件上。还有一个 SNES 控制器作为输入设备的自定义界面。然而，它基本上远远低于最初发布时所要求的规格。他的 8 位 CPU 运行速度仅为 4 MHz，内存为 64 KB。这与最初推荐的运行游戏的 32 位、33 MHz 英特尔 386 芯片和 4 MB 内存相比很差。

[詹姆斯]没有运行真实的东西，而是通过编写自己的演示程序展示了他的机器的局限性，这个演示程序被昵称为*注定*。它能够以 80×60 的分辨率平均输出 19 fps 的视频，由 5000 多行手写汇编代码组成。从根本上说，它是一个基本的 3D 引擎，与 *Wolfenstein* 3D 没有什么不同，尽管没有任何实际的游戏互动。

[詹姆斯]可以简单地说机器不会运行*毁灭*。然而，尝试让类似的东西运行起来是一次有用的学习经历，用他自己的话说，非常令人满意。这种面对逆境勇往直前的态度推动了许多其他的*厄运*移植努力。

 [https://www.youtube.com/embed/OI6Q1r1TxuA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OI6Q1r1TxuA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 Keith Olson 的提示！]