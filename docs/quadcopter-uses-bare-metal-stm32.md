# 四轴飞行器使用裸机 STM32

> 原文：<https://hackaday.com/2019/03/11/quadcopter-uses-bare-metal-stm32/>

[Tim Schumacher]得到了一台 Crazepony Mini 四轴飞行器，并对其进行了“裸机”重新编程——也就是说，他在不使用操作系统或全能环境的情况下对 STM32 进行了编程。他在这个主题上的文章是使用 STM32 和四轴飞行器的很好参考。

如果你没见过四轴飞行器，基本上就是一个带道具的 PC 板。固件是开源的，但是使用 Keil IDE。CPU 是 STM32，具有 64K 的程序存储器。此外，该无人机还配备了无线模块、数字罗盘、高度计和带加速度计的陀螺仪。

虽然这篇文章实际上是关于四轴飞行器的，但[Tim]也给出了关于蓝色药丸的信息，它也可以应用于其他 STM32 电路板。在硬件方面，他使用一个通用的 USB 串行端口和一个基于 Python 的加载器。

在软件方面，他展示了如何设置链接器，并使用 gcc 控制输出端口。当然，其他外围设备还有更多工作要做，Tim 计划调查 CMSIS 以使这项工作更容易。我们之前在 STM32 上的帖子促使[Wassim]在 Hackaday.io 上[回顾了一堆 ide](https://hackaday.com/2017/04/04/hackaday-io-user-reviews-six-stm32-ides/#more-251126)。这也会有所帮助。