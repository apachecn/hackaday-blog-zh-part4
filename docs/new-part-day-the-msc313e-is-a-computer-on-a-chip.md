# 新零件日:MSC313E 是一台片上计算机

> 原文：<https://hackaday.com/2020/04/22/new-part-day-the-msc313e-is-a-computer-on-a-chip/>

随着技术的进步带来了越来越强大的半导体，关注片上系统市场的边缘可能在我们的领域有应用的利基应用设备可能是有益的。Mstar MSC313E 就是这样一款芯片，它是一款专为 ip 摄像机设计的 SoC，内置 ARM Cortex A7 和 64 MB 内存、16 MB 闪存、以太网、USB 和所有其他常见的微处理器接口。它可以在 QFN 的一个包中获得，这使得它很容易被硬件黑客社区获得，所以自然有很大的兴趣去解开它的秘密。一个便宜易得的部件，有足够的能力运行一个精简的 GNU/Linux 操作系统，值得再看一眼！

qfn 不是最容易手工焊接的封装，但如果你也发现自己处于那个位置，至少有一个现成的开发板的前景。 [BreadBee](https://github.com/breadbee/breadbee) 是[一个小 PCB](https://oshpark.com/shared_projects/slorKWK0) ，它封装在芯片中，所有接口包括以太网和 USB，用于实验。如果你不喜欢建造一个，你甚至不必:这是[即将众筹](https://www.crowdsupply.com/daniel-palmer/breadbee)。

有人可能会问，鉴于有太多的 Raspberry-pi 和竞争对手的主板，再推出一个支持 Linux 的微控制器平台有什么意义。答案很简单，其中包含了硬件黑客的本质:*因为它在那里*。除了在几个外围项目中，我们可能再也看不到它了，或者它可能会在我们的世界中找到一个合适的位置并变得流行起来，如果没有这个早期的工作，我们永远不会知道。尽管如此，这并不是第一个这样的 SoC 出现；我们以前见过 action cam 芯片给我们[一台可手工焊接的 Linux 单板计算机](https://hackaday.com/2018/08/12/build-your-own-linux-single-board-computer/)。

谢谢[匿名]的提示。