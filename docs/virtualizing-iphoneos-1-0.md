# 虚拟化 IPhoneOS 1.0

> 原文：<https://hackaday.com/2022/12/25/virtualizing-iphoneos-1-0/>

虚拟化计算机并不是什么新鲜事。然而，苹果设备总是带来挑战。只要问问任何一个开发过黑客电脑的人就知道了。至少计算机硬件通常是暴露的，但在手机上，由于神秘的设备，挑战更加艰巨。[Martijn]成功地对 iPod Touch 1G 进行了逆向工程，足以在其上运行 iPhoneOS 1.0，并发表了几篇博文[解释他是如何做到的](https://devos50.github.io/blog/2022/ipod-touch-qemu/)。

模拟器是无处不在的 QEMU。他对关键硬件进行仿真，包括加密模块、硬件时钟和定时器，以及内存、显示器和接口硬件。然而，Wifi、一些 USB、音频、光传感器和一些图形硬件仍然不存在。然而，这并不能阻止操作系统启动。

这些帖子很好地解释了设备如何启动，显然，openiBoot 项目的代码有助于解决整个问题。它并不完美。例如，键盘会弄坏东西。但这是走到这一步的重要一步。第二篇文章概述了如何建立 QEMU，如果你想自己尝试的话。

一方面，该设备只是另一个 ARM 处理器，QEMU [处理得相当好](https://hackaday.com/2021/04/23/debug-arm-virtually/)。另一方面，所有奇怪的硬件使得模仿、逆向工程或者[甚至修复](https://hackaday.com/2022/05/27/the-huge-apple-toolkit-for-fixing-your-iphone/)变得棘手。