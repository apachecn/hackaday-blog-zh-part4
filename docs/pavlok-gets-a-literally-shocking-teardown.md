# 帕洛克得到了一个真正令人震惊的拆卸

> 原文：<https://hackaday.com/2020/02/02/pavlok-gets-a-literally-shocking-teardown/>

显然，有一种腕戴设备，当它通过蓝牙接收到适当的命令时，就会向佩戴者发出电击。不，这不是某种软禁计划的一部分。如果你相信的话，这个小玩意实际上是用来帮助打破坏习惯或者唤醒极度沉睡者的。我们不知道[贝基·斯特恩]有哪些问题，[，但我们很高兴看到她决定在 21 世纪自我鞭挞开始之前把自己的问题解决掉。](https://beckystern.com/2020/01/28/pavlok-teardown/)

这款名为 Pavlok 的设备在各种在线零售商处售价 180 美元，看起来像一个笨重的健身追踪器。但是代替显示你已经走了多少步或你当前心率的屏幕，有一个闪电按钮，当你想电击自己时，你可以按下它。使用智能手机应用程序，您可以通过一个方便的桌面小工具远程控制设备，该小工具允许您选择电击的强度。不，这不是我们编造的。休息之后，请观看视频，了解实际情况。

[![](img/39e46f8f61348b08472dd361d2997fcb.png)](https://hackaday.com/wp-content/uploads/2020/01/pavlok_detail.jpg) 当【贝基】试图把帕夫洛克拆开时，她发现几乎不可能在不经意间触发电击的情况下处理它。因此，在她能够打开外壳并物理断开电池之前，她所能做的就是降低应用程序的强度，并克服设备偶尔的震动。我们只能希望更多的设备不要采取类似的自我保护意识。

一进去，她就发现了你会在标准的、非受虐的、可穿戴的健身设备中看到的那种硬件。有一个 nRF52832 蓝牙 SoC、一个 MMA8451Q 加速度计、一个 PCF85063A I2C RTC 和一个 FXAS21002C 陀螺仪。然而，你不太可能在 FitBit 中找到的是 LPR6235 耦合电感和大电容，它们用于从标准 3.7 V LiPo 电池中建立高压充电。

我们对最近的项目非常感兴趣，这些项目是[为商用健身可穿戴设备](https://hackaday.com/2019/02/20/custom-firmware-for-cheap-fitness-trackers/)创建定制固件，因为这可能是[获得黑客友好型智能手表](https://hackaday.com/2019/10/07/ask-hackaday-whats-the-perfect-hacker-smart-watch/)的捷径。虽然 Pavlok 有一些引人注目的硬件，并且[Becky]确定的编程标题看起来很有趣，但我们不喜欢成为一个错位的`if`语句而远离闪电的想法。

 [https://www.youtube.com/embed/Fo8H3Ydk3Es?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Fo8H3Ydk3Es?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

