# 电视上的单板电脑

> 原文：<https://hackaday.com/2022/11/14/a-single-board-computer-from-a-tv/>

对于我们社区的一些成员来说，购买一台不是所谓“智能”电视的电视变得几乎不可能，这是一件令人烦恼的事情。这些单元包含一台计算机和显示器，它启动到一个锁定的操作系统，具有用户界面和一系列流媒体应用程序。除了制造商的意图之外，还能对它们做什么呢？[Nina Kalinina]做到了，[从一台废弃的液晶电视中取出主板，并在](https://github.com/ninakali/chip_scavenger/blob/main/src/scavenge/008_tv/index.md)内解放了 ARM Linux 主板。

板上有你期望从电视上看到的所有输入，还有以太网，以及隐藏在 WiFi 接口中的几个额外的 USB 端口。SCART 连接器上有一个 UART，访问 U-boot 菜单是通过使用 Palm Pilot 向红外端口发送字符的不寻常方式实现的。令人惊讶的是，闪存中的设备树是可编辑的，因此，随着 Linux 操作系统的访问，该板显示为具有双核 Novatek SoC。

这让人想起了当年的新热点是从家用路由器中拖出一个 Linux 盒子，就像那些很快被 Raspberry Pi 之类的廉价主板所取代一样，这些电视主板也可能遭遇同样的命运。然而，如果它们可以驱动比电视界面更有用的屏幕，那么这种情况可能会改变，因为谁不想让旧的智能电视更有用一点呢？