# 构建可移植的 Linux 设备:从来没有这么容易过，但仍然很难

> 原文：<https://hackaday.com/2018/11/30/building-portable-linux-devices-never-easier-but-still-hard/>

我们生活在一个单板电脑的黄金时代。曾经有一段时间，一台好的便携式电脑是一种相对罕见和昂贵的设备，当然你不能指望自己复制。一个心灵术士，或者后来的 Palm，或者 WinCE 设备都不仅仅是一时冲动的购买，也不容易用当时实验者可以得到的组件复制。

多亏了为机顶盒和手机开发的技术的衍生产品，我们现在可以购买一堆不同的主板中的任何一个，其功能几乎等同于一台台式电脑。实验者可以利用这种计算能力来创造他们自己的小型便携式电脑。Zerophone 的创造者 Arsenijs Picugins [在最近的 Hackaday 超级会议上谈到了设计 LInux 便携版](https://www.youtube.com/watch?v=gVp5JCB-N2M)的棘手部分。你可以在休息时间下面找到他的讲话，这对于那些想追随他脚步的人来说是一个迷人的入门读物。

![](img/ce742257bd4238c7ad1f94e5bfb15405.png)

[Zerophone](https://hackaday.io/project/19035-zerophone-a-raspberry-pi-smartphone) – a Raspberry Pi Smartphone

## 便携式电脑的小细节是主要的组成部分

从理论上讲，用这种板制作一台便携式电脑非常容易。拿一个树莓派或比格犬骨家族的小成员，加上电池和显示器，你就可以走了。但是魔鬼总是在细节中，对于一个真正成功的构建，有大量的变量需要考虑。

在他的演讲中，Arsenijs 向我们介绍了电源、连接器和接口的挑战。特别是，使用足够小的便携式电池运行 SBC 存在相当大的挑战，因为效率问题和轻松充电的能力构成了一系列重要的选择。然后，我们了解到另一个陷阱，即使用 USB 作为默认接口。在将 5V 电压转换为 3.3V 电压的过程中，功率损耗对于台式电脑来说是无关紧要的，但对于小型设备来说却是电池杀手，因此我们将目光投向了一系列替代方案。

![](img/e1e20715bbf6ad63cbd3ea06ff29c56d.png)

Zerophone screen menu [via [@ZeroPhoneOSHW](https://twitter.com/ZeroPhoneOSHW/status/1049095665224245248)]

## 屏幕尺寸是一个很难解决的问题

如果你已经被那些廉价的树莓 Pi 触摸屏所诱惑，你肯定会明白，虽然在扑克牌大小的屏幕上显示完整的桌面看起来很酷，但实际上几乎无法使用。你的设备将需要一个符合其外形的用户界面，根据他的经验，Arsenijs 建议最好通过按钮而不是较小屏幕上的触摸屏来实现。他向我们介绍了各种各样的 UI 和显示库，使整个过程变得非常简单。

arsenijs '[zero phone Raspberry Pi 智能手机](https://hackaday.io/project/19035-zerophone-a-raspberry-pi-smartphone)是[2017 年 Hackaday 奖](https://hackaday.com/2017/11/10/these-are-the-top-projects-in-the-2017-hackaday-prize/)的决赛选手，并且仍然是一个示范性的便携式项目，许多其他人可以从中获得灵感。我们很荣幸他能把他的经验带到超级大会上来演讲，他的演讲非常精彩。

 [https://www.youtube.com/embed/gVp5JCB-N2M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gVp5JCB-N2M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

