# AIOC:业余无线电音频和 APRS 一体化电缆

> 原文：<https://hackaday.com/2023/01/01/aioc-the-ham-radio-all-in-one-cable-for-audio-and-aprs/>

[业余无线电一体化电缆(AIOC)](https://github.com/skuep/AIOC) 是一个小型 PCB 附件，用于一个流行的无线电收发器系列，增加了一个 USB 连接音频接口和虚拟 TTY 端口，用于编程和一键通功能。STM32F373 微控制器(遗憾的是，在通常的渠道中仍然很难找到)非常适合这种应用，具有所有需要的硬件资源。

通过 USB-C 连接，AIOC 可以列举为一个![](img/ea2446e4d8e20b9fb2174933e247b0fc.png)声卡和一个虚拟串行设备，因此与几乎任何主机的接口都应该是即插即用的。连接到无线电使用 12 毫米分离 3.5 毫米和 2.5 毫米 TRS 连接器，因此至少兼容宝丰 UV-5R，但可能与许多其他具有相同物理设置的廉价收发器兼容。

提供了使用 AIOC 和 [【巨狼】](https://github.com/wb2osz/direwolf) 的说明，以便轻松访问 APRS 应用程序，这是一个很好的开箱即用演示，让您上手。APRS 并不完全是关于跟踪事物的，因为其他应用程序可以位于 APRS/AX.25 网络之上，例如，[【HROT:事物的业余无线电](https://github.com/wb2osz/hrot) 。

我们已经看到了相当多的暴风(和相关产品)黑客，像 [这种粗略的电线堆](https://hackaday.com/2022/11/15/getting-to-the-heart-of-a-baofeng/) 允许一个人为 APRS 试验无线电的胆量。当然，如此廉价的无线电收发器削减了如此多的工程偷工减料，以至于有 [运动禁止其销售](https://hackaday.com/2021/12/05/is-the-game-up-for-baofeng-in-europe/) ，所以也许我们在东方的朋友的一批新的更好的收音机即将出现？

感谢[Hspil]的提示！