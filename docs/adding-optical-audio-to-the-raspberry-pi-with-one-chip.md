# 用一个芯片给树莓派添加光学音频

> 原文：<https://hackaday.com/2021/12/06/adding-optical-audio-to-the-raspberry-pi-with-one-chip/>

在家庭影院领域，大多数人会告诉你光学音频(官方名称为 TOSLINK)的时代已经结束。虽然一度它们是环绕声系统的标准，但带有红色尖端的光纤电缆现在已经在很大程度上被新型电视和音频接收器上的 HDMI 一体化功能所取代。当然，这并不意味着所有的 TOSLINK 兼容硬件都消失了。

如果你正在寻找连接一个树莓 Pi 到你的 AV 系统的光学端口，[【Nick Sayer】已经覆盖了](https://hackaday.io/project/182641-raspberry-pi-toslink-transceiver-hat)。他的“TOSLINK 收发器帽”利用 Cirrus Logic 的 WM8804 芯片从 Pi 的 I [2] S 音频输出到 S/PDIF。信号从那里直接进入 TOSLINK 输入和输出模块，这些模块内置了适当的光纤硬件和驱动器。从软件的角度来看，您只需启用 HiFiBerry 的数模转换器(DAC)的引导覆盖。

[![](img/0c29e3f4aae9c578e4d1cb18352617cd.png)](https://hackaday.com/wp-content/uploads/2021/12/pitoslink_detail.jpg)

The WM8804 is joined by a handful of passives.

说到这里，将这个项目与 HiFiBerry 等公司的商业产品进行比较是不可避免的。虽然我们不能肯定地说[Nick]提出的简单设计与商业市场上更昂贵(甚至更便宜)的选择相比如何，但显然走 DIY 路线总能在 Hackaday 为你赢得额外的分数。另外，[我们一直对解决](https://hackaday.com/2015/06/09/teensy-adds-spdif-to-library/)[消费级光纤技术](https://hackaday.com/2011/06/21/the-engineering-guy-explains-fiber-optics/)这一相对罕见的例子的项目着迷。

[[Nick]在 Tindie 上以 40 美元的价格出售他组装的 TOSLINK 帽子，但他也为任何想自己制作一顶帽子的人提供了所有必要的文件。](https://www.tindie.com/products/nsayer/toslink-transceiver-hat-for-raspberry-pi/)