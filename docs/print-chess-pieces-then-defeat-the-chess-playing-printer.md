# 打印棋子，然后打败下棋打印机

> 原文：<https://hackaday.com/2021/03/06/print-chess-pieces-then-defeat-the-chess-playing-printer/>

象棋无疑是一种精神游戏。可悲的是，当你在电脑屏幕上玩游戏时，一些细微差别就消失了。当一个游戏是触觉的时候，它承载着不同的重力。看一个扑克玩家洗牌，你会发现当一个物理对象在线上时，你就玩了。对 3D 打印并不陌生的[Matou]想要那种触感，但他并没有止步于 3D 打印件。他制作了一些零件来把他的 Creality Ender 3 Pro 变成一个下棋机器人。

为了改装他的打印机，[Matou]设计了一套工具，套在打印头上，将打印头变成一个很酷的夹子。挤压马达现在拉动一根细绳来闭合爪子，这是重新利用该机构的一个非常聪明的方法。一个网络摄像头监视着行动，而机器视觉确定玩家在做什么，然后查询一个[象棋人工智能](https://github.com/thomasahle/sunfish)，并在一个连接的 RasPi 上向 OctoPrint 发送下一步棋。如果两个人有相似的设置，从地球的两端玩触觉象棋应该不是问题。

物理棋子和计算机已经融合了一段时间，可能在设计和游戏性上占据了同等的时间。有几种方法可以像[马头]一样自动移动，或者你可以[让它们与板子](https://hackaday.com/2019/02/09/play-chess-like-harry-potter/)保持接触，然后从下面移动它们。

 [https://www.youtube.com/embed/6b2As388-Ro?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6b2As388-Ro?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

