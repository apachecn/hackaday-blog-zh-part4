# 步进电机分析仪揭示所有

> 原文：<https://hackaday.com/2021/04/23/stepper-motor-analyzer-reveals-all/>

从理论上讲，你真的不需要太多的电子设备。示波器应该做所有的事情。然而，对于特殊用途，使用仪表、逻辑分析仪和其他特殊用途的仪器是很方便的。如果你在 3D 打印机和 CNC 机器等运动系统上工作，你应该有一种看待步进电机的方式。你不知道吗？[Zapta]有一个很棒的[简单步进电机分析器](https://github.com/zapta/simple_stepper_motor_analyzer)，[教学技术] [有一个很棒的视频](https://www.youtube.com/watch?v=4iII25DGIdA)(见下文)，展示了它能做的一些很棒的事情。

它能做什么？它可以就地分析电机，并可以可视化步进、微步和其他操作模式中发生的情况。连接仪器很容易，因为您只需使用一个四针直通连接器。

这个视频很好地解释了步进器是如何工作的，包括看着一个被拆掉的马达，这本身就很有趣。观察微步的驱动波形是展示该工具用途的好方法。

该工具看起来对设置步进驱动电流非常有用，视频显示通过手动调整或使用 g 代码来设置，包括一些热驱动器的热图像。

总的来说，如果你运行步进器，这看起来是一个有用的工具。驱动机器的 CPU 是一个 STM32 " [黑色药丸](https://hackaday.com/2021/01/20/blue-pill-vs-black-pill-transitioning-from-stm32f103-to-stm32f411/)，显然还有一个 TFT 显示屏。一个 EEPROM 和两个电流传感器芯片完善了材料清单。常见问题提到，由于设备有一个 USB 串行端口，所以对固件进行一些更改，如果你想简化项目，你可以移除显示器，只从主机上操作。如果你想了解更多关于驾驶踏步机的艺术，找一个朋友和一辆 555 T3[。](https://hackaday.com/2021/04/09/stepper-motors-quick-and-simple/)

 [https://www.youtube.com/embed/4iII25DGIdA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4iII25DGIdA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

