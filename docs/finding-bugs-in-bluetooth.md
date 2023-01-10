# 35C3:查找蓝牙中的漏洞

> 原文：<https://hackaday.com/2018/12/30/finding-bugs-in-bluetooth/>

[Jiska Classen]和[Dennis Mantz]开发了一个名为 Internal Blue 的工具，旨在成为一把瑞士军刀，用于在较低水平上玩蓝牙。他们的工具基于所有 Broadcom 蓝牙芯片组共有的三个功能:一个让你读取任意内存，一个让你运行它，一个让你写它。嗯，那很简单。他们剩下的工作是分析这些代码，并学习如何用他们自己的版本替换固件。他们花了几个月的时间进行艰难的逆向工作。

最终，Internal Blue 可以让它们在更深的一层(LMP 层)执行命令，从而轻松实现监控和注入。[在一系列的直播中(而且成功了！)演示](https://media.ccc.de/v/35c3-9498-dissecting_broadcom_bluetooth)他们在桌子上的 Nexus 5 的修改版上探索 Nexus 6P。这是他们开始在其他装有 Broadcom 芯片组的设备的蓝牙堆栈中挖掘的地方，也是他们开始发现错误的地方。

[![](img/e8872fd31c6ddd14e60495fa7fb346ae.png)](https://hackaday.com/wp-content/uploads/2018/12/bluetooth_bug.png) 通常情况下，[Jiska]只是四处闲逛，发现了一个不做边界检查的外部代码处理程序。这意味着她可以简单地通过传递~~地址~~处理程序偏移量来运行固件中的其他功能。因为它们本质上是在内存中的任何位置调用函数，所以找到用哪个参数调用哪个函数是一个反复试验的过程，但是这样做的结果至少包括蓝牙模块崩溃和重置，但是也可以使用这样的技巧，例如将蓝牙模块置于“测试设备”模式，这应该只能从设备本身访问。所有这些都是在与设备配对之前完成的——只要走过就足以通过有缺陷的处理程序调用功能。

这种利用的所有细节还不可用，因为 Broadcom 还没有为可能数百万台设备修复固件。他们没有修复它的原因之一是，修补漏洞将揭示所有未修补手机的缺陷所在，并且不是所有供应商都可以同时推出更新。虽然他们专注于 Nexus 5 手机，这是相当旧的，但它适用于任何具有类似 Broadcom 蓝牙芯片组的设备。

除了这里的零日错误，最大的故事是他们的蓝牙分析框架，它肯定会帮助其他研究人员了解更多关于蓝牙的知识，发现更多的故障，并有望帮助蓝牙更公开地受到审查，更安全。现在，任何拥有 Raspberry Pi 3/3+或 Nexus 5 的人都可以将它变成一个低级蓝牙调查工具。

你可能从[她以前的 FitBit 黑客](https://hackaday.com/2017/12/29/34c3-fitbit-sniffing-and-firmware-hacking/)中知道[Jiska]。如果没有，一定要去看看。

 [https://www.youtube.com/embed/4_nI9ok7iQg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4_nI9ok7iQg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

