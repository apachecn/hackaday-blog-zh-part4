# 将廉价的 3D 打印机变成廉价的激光切割机

> 原文：<https://hackaday.com/2018/09/29/turn-a-cheap-3d-printer-into-a-cheap-laser-cutter/>

我们知道这很难接受，但你因为家里有一台 3D 打印机而成为本地黑客空间高手的日子已经一去不复返了。虽然它们仍然是黑客板凳上最挑剔的装备之一，但它们肯定不再是最稀有的了。这些打印机中的一些现在非常便宜，几乎是冲动购买。不管你喜不喜欢，当你告诉别人你已经有了一台个人 3D 打印机时，除了你的祖母之外，很少有人会被打动；如果奶奶在上一次开箱销售中买了一台迷你单价机，我们也不会感到惊讶。

然而，尽管 3D 打印机的所有权不再像过去那样是极客信用的顶峰，但至少还有一线希望:我们可以黑进廉价的运动平台。[【squix】来信告诉我们，他是如何在自己价值 200 美元的 Tevo Tarantula 3D 打印机](https://blog.squix.org/2018/09/how-to-turn-almost-any-3d-printer-into-a-laser-engraver-cutter.html)上安装了一台激光打印机，从而在不倾家荡产的情况下极大地扩展了机器的功能。他的文章中的信息非常广泛地适用于大多数常见的 3D 打印机设计，所以即使你没有狼蛛，适应这个概念也不会太难。

激光器是一个 2.5 W 445 nm 模块，在低成本激光切割机设置中非常受欢迎。这是一个完全独立的风冷装置，只需要一个 12 V 的电源就可以启动。这使得它特别适合改装，因为你不需要硬塞进任何额外的支持电子设备。[squix]只需将它连接到他之前为狼蛛添加的部分冷却风扇的现有电源线上。

在将如此高电流的设备连接到风扇连接器之前，您可能需要检查 3D 打印机控制板的规格。最好的情况是它使电路板的调节器过载并关闭，最坏的情况是魔法烟雾可能会逃逸。明智的预防措施可能是在电路板的风扇输出和激光器之间放置一个 MOSFET，但我们不会告诉你如何生活。就激光安全而言，这种设备可能应该在不透明的盒子里工作，或者在紧闭的门后工作。

一旦激光器挂在打印机控制器的风扇端口上，您可以使用风扇控制的普通 GCode 命令`M106`和`M107`打开它(分别打开和关闭)。你甚至可以通过给“开”命令添加一个参数来控制激光的功率水平，比如:`M106 S30`。

然后你只需要安装激光器，这或多或少是照常营业。控制激光雕刻机/切割机与控制 3D 打印机没有太大区别，所以[squix]仍然使用 OctoPrint 来命令机器；诀窍是给它一个“3D 模型”，这只是一个 2D 图像，没有 Z 的变化要担心。[我们之前已经在 Inkscape 中看到了这样做的过程](https://hackaday.com/2014/01/07/delta-laser-engraver-uses-inkscape-for-g-code/)。

这个激光模块的价格只有 60 美元(假设你有一两台 3D 打印机来进行转换)，这是一种非常便宜的进入减法制造游戏的方式。下一站是[买一辆大家都在谈论的 K40](https://hackaday.com/2018/09/27/laser-noob-getting-started-with-the-k40-laser/)。

 [https://www.youtube.com/embed/B2HojvykQWQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B2HojvykQWQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

