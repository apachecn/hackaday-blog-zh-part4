# 一种面向 FPGAs 的模块化逻辑分析仪

> 原文：<https://hackaday.com/2019/05/26/a-modular-logic-analyzer-for-fpgas/>

当在一个项目中工作时，能够将各种信号可视化是非常有帮助的。当试图确定应该发生的事情是否真的发生时，这一点很重要。然而，逻辑分析仪可能很贵，[因此来自[Bruce Land]的 ECE5760 类的一个小组开发了他们自己的硬件解决方案。](http://people.ece.cornell.edu/land/courses/ece5760/FinalProjects/s2019/amv64_jbc262_nas256/amv64_jbc262_nas256/amv64_jbc262_nas256/index.html)

该项目的主要思想是模块化。逻辑分析仪的基本构建模块用 Verilog 编码。它们的设计使得通道数量和增加的功能可以混合搭配，以适应给定的目的和目标 FPGA 平台的功能。该团队的逻辑分析仪还能够在硬件中解码 SPI 和 I2C，并在连接的笔记本电脑上运行图形用户界面，以可视化信号。

这是一个整洁的构建，也是一个学习 FPGA 编程和各种相关通信协议的基础的极好项目。[布鲁斯·兰德]的课程是 FPGA 项目的温床，从[扑克机器人](https://hackaday.com/2019/05/16/pokerbot-uses-fpga-for-card-calculating-horsepower/)到[NES 芯片模拟器。](https://hackaday.com/2016/06/19/recreating-chiptunes-in-verilog/)休息后的视频。

 [https://www.youtube.com/embed/swHo1FDCt2g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/swHo1FDCt2g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

