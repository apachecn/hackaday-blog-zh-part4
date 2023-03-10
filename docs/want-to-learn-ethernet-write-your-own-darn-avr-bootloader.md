# 想学以太网？写你自己的该死的 AVR 引导程序！

> 原文：<https://hackaday.com/2018/10/30/want-to-learn-ethernet-write-your-own-darn-avr-bootloader/>

有一个学派认为，要完全理解一件事，你需要自己去构建它。好吧，我们不确定这是否真的是一个思想流派，但这描述了围绕这些部分的大量项目。

[Tim] aka [mitxela]写了 [kiloboot](https://mitxela.com/projects/kiloboot) 部分是因为他想要一个支持以太网的普通文件传输协议(TFTP)引导程序用于 ATMega 驱动的项目，部分是因为他想了解互联网。看，如果你正在写一个 bootloader，你只有有限的空间，也没有任何类型的设备驱动程序或库可以依靠，所以你要学习你选择的主题。

[Tim]写的将如此多的东西塞进 1000 字节的代码的冒险历程非常精彩。虽然解释互联网比以太网功能的引导程序本身占用更多的空间，但我们敢打赌，你会像我们一样喜欢 UDP、IP、TFTP 和 AVR 引导程序的压缩概述。是的，在一天结束时，你还会有一个可上网的 Arduino，如果你正在构建一个简单的有线物联网设备，并且厌倦了跑到地下室上传新固件，这正是医生所订购的。

哦，如果你没有注意到，把一个以太网引导程序塞进 1 kB 是惊人的。

说到引导加载程序，如果你正在用一个 ATtiny85 构建一个 I2C 从设备，你会想看看这个运行在微型芯片上的引导加载程序。