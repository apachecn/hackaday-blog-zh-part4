# 挠痒痒

> 原文：<https://hackaday.com/2020/10/31/scratching-that-itch/>

我做了件蠢事。我在易贝买了十架“坏”的劣质室内四轴飞行器——希望能凑成一架能用的，逗我儿子开心。在这一点上，我有八个工作。坏消息是，它们都带有非常便宜的发射器，根本不利于飞行。如果能用一个真正的遥控器来控制它们，那会有趣得多。黑客进入。

几乎所有的廉价四轴机都是基于少数无线电芯片组中的一种，尽管它们使用不同的协议。一个有事业心的黑客可以想象得到只是将这些无线电模块捆绑在一起，剩下的就是简单的软件问题了。这正是 Pascal Langer 的 [DIY 多协议 TX](https://github.com/pascallanger/DIY-Multiprotocol-TX-Module) 和支持固件所做的。这个爱好项目非常成功，兼容的硬件由不少中国公司生产，非极客也将它们安装在他们的收音机里。该模块可让您控制几乎任何使用 2.4 GHz 的设备。当然，我有一个。

[![](img/b8cc5fe4b56ef69acae6cf6a90d34a3d.png)](https://hackaday.com/wp-content/uploads/2020/10/DSCF1972_thumbnail.png) 我打开了 cheesy drone 的发射器，发现它使用了一种流行的芯片组，并通过了所有使用它的不同支持协议。没有骰子。但是无线电模块*和*有很好的标记 SPI 线路，所以我联系了 Pascal。几个 [Sigrok](https://sigrok.org/) 会话之后，他发现它试图绑定到一个不同的频道，我重新编译了固件，并在玩无人机的其他功能。

我只是喜欢好的 [SPI 嗅探会话](https://hackaday.com/2016/07/01/what-could-go-wrong-spi/)。`sigrok-cli -d fx2lafw -c samplerate=4000000 -P spi:clk=D0:mosi=D1:cs=D2 -A spi="mosi transfer" --continuous | grep A0 | uniq`实时读取 SPI 线路、解码数据包、过滤命令并删除重复内容。剩下要做的就是摇动棍子，捣碎按钮，做好笔记。

这些都不难，当然也不贵。我让我的无人机在我的花哨的遥控器的控制下，并且由于每个人之前对这些协议的逆向工程工作，我后来在算法上控制它们有了一个很好的立足点。对 DF Drone 的 SkyTumbler 的支持将包含在下一个 DIY 多协议 TX 版本中，我在这个项目上度过了大约四五个愉快的小时。也许只有少数人会偶然发现这个特殊的协议——或者可能只有我。我这么做主要是为了搔自己的痒处。

但这是开源工作、繁荣和发展的一种方式。这是给你们所有人的，从[偏差](https://deviationtx.com/)团队，他们做了许多早期无人机协议逆向工程，到 Pascal 的 DIY 模块，到 Sigrok 的人，他们让我可以使用工具，以借鉴每个人以前的工作。继续黑！

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!