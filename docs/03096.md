# 让 8 位国际象棋游戏对抗现代敌人

> 原文：<https://hackaday.com/2019/05/23/pitting-8-bit-chess-games-against-modern-foes/>

UltraChess 是一款适用于 8 位 MSX 平台的经典国际象棋游戏，在 Z80 上运行。[flok]想知道这款游戏到底有多强，[并着手在其他各种国际象棋引擎上测试它。](https://vanheusden.com/misc/blog/2018-09-08.php)

UltraChess 设计于 20 世纪 80 年代，就国际象棋软件世界而言，它远远不是最新的。通过使用 OpenMSX 模拟器来运行游戏，[flok]能够实现脚本来读写 UltraChess 中的 gamestate，并使其与[通用象棋接口](https://en.wikipedia.org/wiki/Universal_Chess_Interface)兼容。这将允许超级国际象棋与各种其他国际象棋引擎进行比赛，以确定其近似的 [ELO 等级](https://en.wikipedia.org/wiki/Elo_rating_system)。

这些脚本运行得很好，并且可以在 Github 上找到，供那些希望进一步修补的人使用。不幸的是，[flok]至今无法确定 UltraChess 的评级，因为它在与其他国际象棋引擎的比赛中输掉了每一场比赛。鉴于有限的处理能力，这并不奇怪，但我们希望看到一个经过调整和改进的 Z80 国际象棋程序来应对同样的挑战。如果你做过这样的事情，[让我们知道](http://hackaday.com/submit-a-tip)，或者[你可能会喜欢像哈利·波特那样玩。](https://hackaday.com/2019/02/09/play-chess-like-harry-potter/)