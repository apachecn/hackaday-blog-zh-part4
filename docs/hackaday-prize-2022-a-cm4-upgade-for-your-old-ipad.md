# Hackaday Prize 2022:为您的旧 IPad 进行 CM4 升级

> 原文：<https://hackaday.com/2022/06/27/hackaday-prize-2022-a-cm4-upgade-for-your-old-ipad/>

市面上不乏制作精良的平板电脑，但不幸的是，其中许多都采用了目前已经严重过时的主板。由于制造商为他们的旧硬件发布替换主板看起来不太可能很快成为惯例，社区将不得不自己动手。这就是[Evan]的项目的切入点——[为最初的 iPad 设计一个基于 Raspberry Pi CM4 的主板](https://hackaday.io/project/177256)。它旨在支持你所期望的一切:显示器、触摸屏、音频、WiFi、蓝牙，甚至是 dock 端口。此外，它给你更多的计算能力来充分利用它。

[![](img/f143b44d2dd3c221e570a825dfb9095e.png)](https://hackaday.com/wp-content/uploads/2022/06/pipad_detail.jpg)

Testing part fitment with some cardboard CAD.

最初的 iPad 做了很多正确的事情，这无疑是它发布时取得成功的一个因素。[Evan]的高努力改造与 iPad 的大量好部件一起工作，如其坚固的外壳、定制的锂离子电池、对眼睛友好的 LCD 和可靠的电容式触摸屏。你必须在这些部件组装在一起后，在可用的空间内安装新的主板，而[Evan]已经对他的 PCB 进行了改造，以实现这一点——为 CM4 和他添加的众多 IC 留出空间，以便没有功能未实现。

这个项目已经进行了一年多，目前，有[14 个信息密集的工作日志](https://hackaday.io/project/177256/logs?sort=oldest)讲述这个改造的故事。对电容式触摸屏和 LCD 进行反向工程，为所有定制连接器制造突破，集成定制音频编解码器，调试设备树问题，以非常规方式访问意外断开的 QFN 引脚，以及广泛的电源管理设计之旅。[Evan]对于希望更新旧平板电脑的人来说，有很多东西可以教！

硬件文件[是开源的，](https://github.com/EvanKrall/pipad)为其他人重新使用部件进行改造铺平了道路，我们绝对希望看到更多像这样的改造。这个项目是 2022 年 Hackaday 奖[*Hack it Back*回合](https://hackaday.com/2022/06/13/2022-hackaday-prize-hack-it-back-and-make-it-yours/)的一部分，看起来非常适合我们。如果你正在寻找一个开始类似项目的借口，现在正是时候。

The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)