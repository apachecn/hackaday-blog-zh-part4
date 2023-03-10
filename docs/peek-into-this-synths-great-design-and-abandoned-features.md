# 窥视这个 Synth 的伟大设计(和被放弃的功能)

> 原文：<https://hackaday.com/2021/03/09/peek-into-this-synths-great-design-and-abandoned-features/>

[Tommy]的 [POLY555 是一个模拟的 20 音符复音合成器](https://blog.tommy.sh/posts/poly555-synth/)，它大量使用 3D 打印并展示了一些巧妙的设计。POLY555 以及[Tommy]早期的 synth 设计都是基于 555 定时器。但是一个 555 是一个振荡器，也就是说一次只能弹一个音符。为了使 POLY555 复音，[Tommy]将事情发挥到了逻辑的极致，简单地添加了多个 555，在保持经典 555 synth 传统的同时扩展了功能。

[![](img/5b3fb2822c4159cf3985bdb867518b8f.png)](https://hackaday.com/wp-content/uploads/2021/03/poly555_branding.jpg) 这里真正的精华是【汤米】的文章。在这篇文章中，他解释了 POLY555 的各种设计选择和改进，不仅仅是作为一种乐器，而是作为一种易于生产和组装的套件。好的 DFM(可制造性设计)需要时间和努力，但即使是相对少量生产的产品也能获得巨大的时间回报。任何降低复杂性、消除步骤或提高可靠性的变化都值得研究。

例如，音量轮不是指轮壶。它实际上是一个 3D 打印件，连接到 555s 用于调谐的同一电位计上；这意味着物料清单中少了一个需要跟踪的部分。这是一个技巧的金矿，对于那些不仅仅想做一些东西的人来说，也是一个窥视设计要生产的东西的艰苦工作的机会。[Tommy]甚至有一小段是专门用来介绍那些没有通过的被放弃或拒绝的想法的，这本身就很有教育意义。想要更多吗？好消息！[这不是我们第一次对[Tommy]的原型和设计讨论感到高兴](https://hackaday.com/2018/03/30/learn-what-did-and-didnt-work-in-this-prototyping-post-mortem/)。

POLY555 的设计文件(外壳和零件的 OpenSCAD，原理图和 PCB 的 KiCad)以及组装指南[都可以在 GitHub](https://github.com/oskitone/poly555) 上找到，STL 文件可以在 [Thingiverse](https://www.thingiverse.com/thing:4676728) 上找到。[Tommy]还出售部分和完整套件，因此每个人都有自己满意的产品。观看下面嵌入的视频中的 POLY555。

[https://player.vimeo.com/video/495255208](https://player.vimeo.com/video/495255208)