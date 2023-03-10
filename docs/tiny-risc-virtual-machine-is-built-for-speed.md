# 微型 RISC 虚拟机专为速度而生

> 原文：<https://hackaday.com/2022/04/28/tiny-risc-virtual-machine-is-built-for-speed/>

我们大多数人都熟悉虚拟机(VM ),它是一种测试各种操作系统、可靠地部署服务器和其他软件或防范潜在恶意软件的方法。但是虚拟机并不局限于运行完整的服务器或桌面操作系统。[这款微型虚拟机能够在 Raspberry Pi 或 AVR 微控制器等功能较弱的系统上部署软件](https://hackaday.io/project/163741-l1vm),而且速度非常快。

虚拟机是从零开始构建的，包括只有 61 个操作码的 RISC 处理器，一个 64 位核心，并运行用他自己的编程语言编写的代码，称为“括号”或汇编。它被设计成模块化的，所以只有给定应用程序需要的东西才被加载到 VM 中。根据这些设计标准，它的速度比 NanoVM 等相对较小的虚拟机快 7 倍。该项目的创造者[koder77]甚至使用其直接鼠标读数和操纵杆功能来控制 Raspberry Pi 3D 摄像机器人。

对于任何希望在小型计算环境中添加高效虚拟机的人来说，[koder77]已经在他的 GitHub 页面上开源了这个项目[。这还包括他迄今为止创建的所有模块，这些模块极大地扩展了项目的功能。为了进一步了解超小型虚拟机，](https://github.com/koder77/l1vm)[我们在 2012 年](https://hackaday.com/2012/10/15/%CE%BCj-a-java-virtual-machine-for-microcontrollers/)介绍了这个项目，它允许用户在相似的硬件上运行 Java。