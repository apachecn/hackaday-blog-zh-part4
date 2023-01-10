# 桌面图灵机魔术:收集卡片

> 原文：<https://hackaday.com/2019/07/18/a-card-table-top-turing-machine-of-magic-the-gathering-cards/>

在收藏卡牌游戏的常规规则中*魔法:聚集*玩家可能会发现自己只能采取一种合法的行动。这种情况下，玩家可以策划挫败他们的对手，尽管受害者通常在几个动作后就会挣脱。但是在精心设计的场景下，玩家将别无选择，只能通过本文详述的技术成为用*魔法*卡片[编写的图灵完全编程语言的执行引擎。](https://arxiv.org/abs/1904.09828)

这篇论文的作者之一，[ [亚历克斯·丘吉尔](https://www.toothycat.net/~hologram/Turing/About.html) ]于 2010 年开始致力于这项挑战。我们在这里报道了[的早期作品](https://hackaday.com/2012/09/12/building-a-turing-machine-from-magic-the-gathering)，以及[自己的批评](https://www.toothycat.net/~hologram/Turing/Future.html#Future)，他认为这依赖于玩家的合作。在不同的点上，游戏规则规定玩家“可以”采取某些行动，如果我们的玩家选择了错误的东西，这个结构就会崩溃。这就好像一台计算机是由晶体管组成的，这些晶体管“可能”根据命令或不根据命令进行切换，这不是一种非常可靠的计算方法。

为了提高这种特殊图灵机执行引擎的可靠性，该团队梳理了规则和卡片，以设计一种编码，其中玩家只能看到一条合法的前进路线。这确保了指令流的确定性执行，现在有了图灵完全性的证明，我们祝贺[Alex]十年的探索获得了成功。

我们为任何想重温图灵机的人准备了一本入门书。它们完全不切实际，但对黑客来说很有趣，它们通常由[电子设备](https://hackaday.com/2016/07/12/a-very-modern-turing-machine-build/)和[发光二极管](https://hackaday.com/2018/02/23/a-two-tapes-turing-machine/)组成，而不是纸板上的墨水。

通过 Ars Technica，他们提出了自己对这台机器的分析。

主图:未指定的一套[魔法:由【罗伯特】](https://www.flickr.com/photos/jemimus/14695910586) [CC 由 2.0](https://creativecommons.org/licenses/by/2.0/) 收集的卡片