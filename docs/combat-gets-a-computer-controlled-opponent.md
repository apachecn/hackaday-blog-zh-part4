# 战斗得到一个电脑控制的对手

> 原文：<https://hackaday.com/2022/08/01/combat-gets-a-computer-controlled-opponent/>

如果你曾经在 Atari 2600 上玩过一段时间，你很有可能经历过几轮*战斗*。这款双人对战游戏不仅配备了主机，而且实际上是该系统中技术上更令人印象深刻的游戏之一，提供了近 30 种核心一对一游戏模式的变体。

但不幸的是，这些模式都不包括单人游戏。也就是[直到【尼克·比尔德】上了案](https://github.com/nickbild/combat)。虽然不得不做出一些让步，但他在最初开发者失败的地方取得了成功，并在*战斗*中添加了一个电脑控制的敌人。此外，游戏仍然可以在 stock 2600 硬件上运行——不需要模拟器技巧。真正的爱好者可能会对他提供的源代码片段感到惊讶，但我们其他人可以只看休息时间下面的视频，并对这一成就感到惊讶。

[![](img/d7b70c3cd83b9c252749f8a45fa1676a.png)](https://hackaday.com/wp-content/uploads/2019/11/argos-bod-atari-2600.jpg) 如果你从未在这样一个受约束的系统上工作过，这可能看起来没什么大不了的。但是[尼克]不仅很好地解释了他的所作所为，还解释了当初为什么这么难成功。例如，主机没有视频缓冲区，所以一切都需要在 VBLANK 期间完成，游戏不需要绘制到屏幕上。不幸的是，这没有给他足够的空闲周期，所以他不得不将代码分割成三个框架，而不是一个框架。这意味着最初的游戏逻辑现在每秒只运行 30 帧中的 27 帧，但他说你在实践中真的看不出来。

也就是说，必须进行一些削减。他需要消除令人惊讶的复杂引擎声音以释放一些资源，并且必须将 2 KB 的磁带提升到 4 KB 以容纳新的代码和数据。原来 2600 可以处理更大的墨盒通过银行切换，所以这实际上不是一个问题。

考虑到它的年龄和与更现代的游戏机相比有限的功能，你可能会认为 Atari 2600 只不过是游戏史上的一个脚注。但是有一群忠心耿耿的人喜欢从系统 45 年的硬件中榨出他们能榨出的一切，这[导致了像这样的爱的劳动](https://hackaday.com/2019/04/22/get-coding-with-this-atari-2600-development-suite/)。

 [https://www.youtube.com/embed/gU0H_XM2bXk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gU0H_XM2bXk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

