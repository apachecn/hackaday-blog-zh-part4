# kvm 使用许多 arduino

> 原文：<https://hackaday.com/2020/04/19/kvm-uses-many-arduinos/>

Arduino 平台是最通用的微控制器板之一，有各种各样的形状和尺寸，非常适合从闪烁的几个 led 到机器人到整个家庭自动化系统。它的一个更微妙的特性是能够使用它的串行库来处理键盘和鼠标的任务。虽然这可以用于基本的 HID 实现，但[Nathalis]更进一步，[使用一系列 Arduinos 作为 KVM 开关](https://github.com/nathalis/Arduino-KVM-Switch)；虽然不可否认没有视频和鼠标功能。

首先，Arduino Uno 接受来自键盘的输入，该键盘处理来自键盘的输入串行信号。从那里，两个 Arduino Pro 微型计算机并行连接，并接收来自 Uno 的信号，以发送到各自的计算机。scroll lock 键是两个输出之间的切换开关，在现代除了打乱 Excel 电子表格之外，它没有什么作用。一切都是标准的 USB HID，所以它应该兼容几乎所有的东西。所有的源代码和图表都可以在项目的资源库中找到，任何人都可以在家一起玩。

使用 Arduino 来模拟 USB 输入设备并不一定要只工作不玩耍，相同的基本概念[也可以用于构建定制的游戏控制器](https://hackaday.com/2020/03/11/custom-tibia-keyboard-for-a-leg-up-in-the-game/)。