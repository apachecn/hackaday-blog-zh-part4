# 游戏卡带并不像你想象的那么简单

> 原文：<https://hackaday.com/2019/09/19/that-game-cartridge-isnt-as-straightforward-as-youd-think/>

经典游戏控制台从盒式磁带上玩游戏，盒式磁带是一种塑料砖块，上面有一个 PCB，上面有游戏代码，可以由控制台硬件运行。鉴于代码可以从它们所包含的任何 rom 中提取出来，因此您可能会认为它们是一个容易模仿的对象。但是任何对此感兴趣的人都会告诉你，一些卡带包含了额外的硬件来增强游戏的性能，这使得模拟器的工作变得更加复杂。

[Byuu] [已经写了一篇文章来探讨这个主题](https://byuu.net/cartridges/boards)跨越各种各样的控制台，深入分析了特殊情况的墨盒。我们看到了一些明显的例子，如一些 SNES 游戏中著名的 DSP 协处理器，以及任天堂的超级游戏机，它在一个芯片上包含了整个游戏机。

但也许更有趣的是不包含特殊硬件的边缘盒。Capcom 的 *Rockman X* 有一个复制保护功能，如果它在一个频繁使用的保存游戏地址检测到内存，就会破坏游戏。不幸的是，这也可能被意外触发，所以每一个第一代*洛克人 X* 墨盒都有一个手动连接的博奇线，一个忠实的仿真器必须复制。还有世嘉创世纪 *F22 拦截器*的情况，它包含一个 8 位 ROM，这个 68000-powered 平台的大多数墨盒都有一个 16 位的部分。由于浮动数据线的原因，复制该盒式磁带的简单尝试会导致高 8 位具有随机值，仿真器必须正确处理这种情况。

这是一个种类繁多的主题，就像游戏机开发者及其游戏的数量一样庞大，也是一个新的怪癖不断被挖掘出来的领域。虽然我们大多数人不会把时间花在盯着积满灰尘的墨盒上，但我们很感激这种对那个世界的洞察。

我们之前已经访问过几次模拟器的世界，例如当我们看着对抗游戏中的延迟时。