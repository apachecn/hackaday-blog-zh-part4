# Arduino 使您的经典 Timex 数据链路保持同步

> 原文：<https://hackaday.com/2022/03/26/arduino-keeps-your-classic-timex-datalink-in-sync/>

Timex Datalink 可以说是第一款可用的智能手表，美国国家航空航天局(NASA)的宇航员以及比尔盖茨(Bill Gates)等极客偶像都戴着它。它可以存储闹钟、提醒和电话号码，当然还可以显示几十个时区的时间。数据链的主要创新之一是它能够从你的个人电脑上下载信息——或者通过 CRT 显示器上闪烁的图像，或者通过插入串行端口的特殊适配器。

随着 CRT 在地面上变得越来越薄，原始的串行适配器在网上卖到了可笑的价格，今天的经典数据链用户可能会发现很难让他们的手表与他们的 Outlook 日历保持同步。幸运的是，[famiclone]提出了一个解决方案:[一个基于 Arduino](https://github.com/famiclone6502/DIY_Datalink_Adapter) 的 DIY 数据链适配器。它的工作方式与 Timex 的串行适配器相同，即它通过计算机的串行端口接收数据，并通过闪烁红色 LED 将数据传输到手表。

更新您的手表需要使用原始的 Datalink PC 软件，该软件只能在 Windows 95 或 98 等经典操作系统上运行，因此您需要保留一份这样的操作系统的副本。幸运的是，它与虚拟机或 USB 通信端口没有问题，所以至少你不需要保留老式的 PC 硬件。话说回来，拿出一台 1995 年的奔腾笔记本电脑来更新你的 Timex 手表，将是一场终极的极客派对。

喜欢经典的极客手表？看看几年前我们对他们做的这篇专题文章。如果你对使用电脑显示器进行光学数据传输感兴趣，我们已经报道了[几个](https://hackaday.com/2011/12/22/microcontroller-comm-with-a-computer-monitor/) [项目](https://hackaday.com/2011/07/28/microcontroller-communications-using-flashing-lights/)可以做到这一点。