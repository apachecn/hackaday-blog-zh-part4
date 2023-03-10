# 家酿 RISC-V 电脑有美貌有头脑

> 原文：<https://hackaday.com/2021/04/13/homebrew-risc-v-computer-has-beauty-and-brains/>

构建自己的 CPU 可以说是真正理解计算机中所有这些 1 和 0 是如何被抛出的最佳方式，但正如你可能想象的那样，即使是一个相对简单的处理器也需要惊人的时间和耐心来组装。此外，通常情况下，你会留下一个电线和电路板的迷宫，占据了你桌子的一半，除了让一些发光二极管闪烁之外，你什么也做不了。

[![](img/39cbb13558b07ec39a64d782ca6969a6.png)](https://hackaday.com/wp-content/uploads/2021/04/diyriscv_detail.jpg)

An early prototype of the Pineapple ONE.

但是由菲利普·斯坎德拉制造的菠萝电脑不是普通的自制电脑。当然，他仍然花了两年时间来设计、调试和组装他的 32 位 RISC-V CPU 和所有相关硬件；但最终的结果是一台看起来很棒的机器，它运行 C 程序，并在 VGA 上提供一个基本的交互式外壳。事实上，凭借其光滑的 3D 打印外壳、垂直堆叠的结构和模块化的外围连接，它看起来更像某种高科技科学仪器，而不是计算机；自制或其他。

[Filip]说，他的灵感来自于[Ben Eater]著名的 8 位试验板计算机和[Robert Baruch]的 LMARV-1(给我学一个 RISC-V，第 1 版)，他只用分立逻辑元件就能制造出这种 500 kHz(是的，千赫兹)的美。他花了六个月的时间模拟机器，然后才开始创建原理图，更不用说设计各个电路板了。他试图将所有 PCB 保持在 100 x 100 mm 以下，以利用制造商的折扣，最终决定将九块电路板垂直对齐，并用引脚接头连接在一起。

在下面的视频中，你可以看到[Filip]启动了计算机，调用了一些系统信息，甚至在偷看和拨弄机器的 512 kB RAM 之前玩了一个基本的贪吃蛇游戏。听起来似乎还有一些工作要做，还有一些错误要克服，但是我们已经看到了足够多的东西，可以说这台机器已经进入了大师级自制计算机的殿堂。

 [https://www.youtube.com/embed/NUAVKNVrPh0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NUAVKNVrPh0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

