# 最意想不到的平台——任天堂 64 的全新 Linux

> 原文：<https://hackaday.com/2021/01/01/a-fresh-linux-for-the-most-unexpected-platform-the-nintendo-64/>

尽管 Linus Torvalds 以“*一个(免费的)操作系统(只是一个爱好，不会像 gnu 一样庞大和专业)而闻名于世，但 Linux 内核和周围的操作系统生态系统已经被移植到 x86 之外的许多架构上。因此，听到不支持平台的新端口并不罕见，但当平台是 20 世纪 90 年代中期的游戏主机时，听到这种新端口是非常意外的。但这就是[劳里·卡萨宁]所做的，[宣布为任天堂 64](https://lore.kernel.org/linux-mips/20201225190503.12353218812e1655f56f0bf8@gmx.com/T/#m0862c3484e0da7195dc8989421d30f01b3b1c63a) 提供一个新的 Linux 端口。*

这也不是 1996 年的 Linux。该移植建立在最新的内核版本 5.10 上，带有他的 N64 分支，并且有可能被集成到 MIPS-64 处理器架构的主要 Linux 源代码中。没错，任天堂 64 可能是官方支持的 Linux 平台。

如果把它称为任何一种发行版，那就太牵强了，因为他制作的是一个引导加载程序，它加载内核并创建一个加载了 busybox 的终端。有了它，你不会很快取代那个树莓派，所以除了[Lauri]的"*因为我可以*"你会对它感兴趣吗？他给出了答案，答案就在仿真场景中，因为有了 Linux 平台，移植其他软件就容易多了。如果这引起了你的兴趣[，你可以在他的 GitHub 库](https://github.com/clbr/n64bootloader)中看到源代码，我们当然期待社区会用它做什么。

我们更习惯于将 N64 视为机箱改造的主题，[无论它是作为一款手持设备](https://hackaday.com/2020/12/25/is-this-the-worlds-smallest-nintendo-64/)还是作为一款多功能控制台的[。](https://hackaday.com/2019/12/15/the-boxy-all-in-one-nintendo-64-your-1990s-self-always-wanted/)

Via [Phoronix](https://www.phoronix.com/scan.php?page=news_item&px=Nintendo-64-Linux-2020-Port) ，感谢【David Beckershoff】的提示。

头图:埃文-阿莫斯，[公共领域](https://commons.wikimedia.org/wiki/File:Nintendo-64-wController-L.jpg)。