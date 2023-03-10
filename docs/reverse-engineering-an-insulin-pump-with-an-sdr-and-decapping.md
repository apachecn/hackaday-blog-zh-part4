# 对带有 SDR 和去盖的胰岛素泵进行逆向工程

> 原文：<https://hackaday.com/2019/04/29/reverse-engineering-an-insulin-pump-with-an-sdr-and-decapping/>

胰岛素泵是糖尿病患者使用的一种医疗设备，用于自动将定量的胰岛素输送到血液中。传统上，它们包括一个导管和单独连接的泵，但最近的模型采取了贴片的形式，泵直接安装在贴片上。当[皮特·施瓦姆]的女儿收到这些泵中的一个，一个 Omnipod 泵时，他回应了一项对其射频协议进行逆向工程的悬赏。作为帮助创建用于控制胰岛素输送系统的应用程序框架[循环](https://loopkit.github.io/loopdocs/)的人员之一，他特别适合做这项工作。

逆向工程本身始于一个熟悉的故事，即使用 SDR 窃听设备在泵和控制设备之间的 433MHz 通信。查询原始数据很简单，但是理解它却不容易。该设备使用的 CRC 算法存在问题，该算法有一个错误，涉及到错误方向的按位移位，然后他们在数据加密中遇到了阻力。硬件调查显示，该设备中有一个定制芯片，它们可能就停在那里。

但是国际逆向工程界并不是没有资源和专业知识，通过英国一名大学研究人员令人难以置信的工作(他的论文顺便包括了一个泵的拆卸)，他们能够在许多人的支持下，通过解封芯片来恢复固件。即使他们这样提取了加密代码并制作了自己的软件，他们的问题也没有结束，因为通信问题需要在 [RileyLink](https://loopkit.github.io/loopdocs/setup/requirements/rileylink/) 蓝牙桥接板上安装更好的天线，将蓝牙从手机转换到 433 MHz。

这份摘要并没有完全囊括一大群具有非常专业的技能的人在几年内对 Omnipod 进行逆向工程所做的大量工作。成功完成这项任务是一个不可思议的壮举，也是一篇引人入胜的报道。

谢谢[亚历克斯]的提示。