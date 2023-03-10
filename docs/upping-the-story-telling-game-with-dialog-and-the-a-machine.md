# 用对话和机器升级讲故事游戏

> 原文：<https://hackaday.com/2019/09/16/upping-the-story-telling-game-with-dialog-and-the-a-machine/>

自从 Infocom 发布了他们的互动故事游戏 *Zork* 并因微型计算机而获得世界范围的好评以来的几十年里，互动小说(IF)这种类型仍然非常受欢迎，数量惊人的现代 IF 作品针对 Infocom 最初用于 8 位微型计算机的 Z-Machine 运行时。这些年来，随着[【莱纳斯·奥克森】的对话语言](http://www.linusakesson.net/dialog/index.php)的出现，我们已经看到了许多针对该平台的运行时和语言的改进。

在 IntFiction 的[这个主题中，涵盖了关于这种语言的技术细节，这种语言有趣的一面是，虽然它有一个编译器将它编译成 Z-Machine 的 Z 代码，但[Linus]还实现了一个新的运行时，称为“](https://intfiction.org/t/dialog/13922)[机器](http://www.linusakesson.net/dialog/aamachine/index.php)”，因为在字母表中“o”跟在“Z”后面(如果你是瑞典人，就是这样)。这个运行时应该允许更大的故事和其他更好地利用更多资源的特性，同时仍然允许较小的故事在旧硬件上工作。不幸的是，目前唯一的机器实现是用 JavaScript 编写的，不知道它在 Commodore 64 甚至 Amiga 500 系统上是否能很好地工作。

至于 Dialog 本身，[它的文档](https://linusakesson.net/dialog/docs/index.html)提供了该语言能力的详细概述，据称是受到了 [Inform 7](http://inform7.com/) 和 [Prolog](https://en.wikipedia.org/wiki/Prolog) 的启发。它的目标是易于理解，具有最少的语言概念和高性能。正如文档中提到的，由于缺乏优化，许多基于 Z-Machine 的故事在老式硬件上无法播放。

不久前，我们详细介绍了 Zork 和 Z-Machine 。我们很高兴看到人们对这个平台仍有如此大的兴趣。也许有一天会有人为 Commodore 或 MSX 系统编写一个-Machine 实现，看看它与 Infocom 的 Z-Machine 相比如何。为卓克家族的下一个几十年干杯。