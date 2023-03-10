# Arduino +业余无线电=发短信

> 原文：<https://hackaday.com/2021/11/19/arduino-ham-radio-texting/>

在 Spectrum 网站上，[Dale]——一个相对较新的业余无线电爱好者——谈论他的通过甚高频无线电发送文本消息的系统，该系统被称为[业余无线电爱好者](https://spectrum.ieee.org/ham-radio-text-hacking)。当然，hams 一直使用各种协议发送信息，但是[Dale]想要一个自带键盘、屏幕和 GPS 接收器的便携式设备。所以他造了一个。你可以在 [GitHub](https://github.com/dalethomas81/HamMessenger) 上找到他的作品。

该项目的核心是 MicroAPRS，一种用于分组无线电的 Arduino 固件。他没有使用更大的计算机，而是决定用另一个 Arduino 来做除了调制解调器功能之外的所有事情。

剩下的你大概能想出来。一个 10 美元的 GPS，一个电池组，一个充电控制器，以及一些用户界面部件，如有机发光二极管屏幕和键盘。此外，还有一个 SD 卡来存储信息。

当然，我们不禁注意到我们的手机有键盘、屏幕、GPS 和存储器。我们可能会想出一种通过蓝牙将收音机连接到它的方法。但我们不得不承认，这个小 HamMessenger 装置看起来很酷，充电时间可能也比我们的手机长。