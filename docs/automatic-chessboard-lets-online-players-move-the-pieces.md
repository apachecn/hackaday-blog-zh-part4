# 自动棋盘让在线玩家移动棋子

> 原文：<https://hackaday.com/2021/06/10/automatic-chessboard-lets-online-players-move-the-pieces/>

在网上下棋是很好的，它打开了一个竞争者的世界，否则在一个人的本地是无法获得的。但是对于玩棋盘游戏还是有一些要说的，这对于很多玩家来说经常出现，以至于他们用首字母缩写 OTB 来指代它。[【卡洛斯】建造了一个名为幻影的自动棋盘，旨在连接从网络空间到现实空间的不同国际象棋世界。](https://hackaday.io/project/179268-automatic-chessboard)

![](img/cd551f13ecd98ab2a9a1b78911d6ae32.png)

The Phantom board in action.

基本的想法是一个棋盘，玩家可以以典型的方式使用，像平常一样移动棋盘上的棋子。然后，对方棋子自动移动，以反映从在线象棋服务器接收到的对方玩家的移动。

董事会表面上看起来很正常，没有什么不妥的地方。只有每件作品底部的金属闪光泄露了秘密。棋子由藏在棋盘内的 SCARA 臂移动，它使用磁铁将它们从一个位置拖到另一个位置。看着棋子像被施了魔法一样四处滑动是很有意思的，尤其是当一个人在战斗中被拖下棋盘的时候。

至于控制系统，Arduino Nano 33 物联网处理在线连接，从 Lichess chess 服务器获取游戏数据，而 ESP32 负责所有电机，常规 Arduino Nano 扫描霍尔效应传感器矩阵，负责定位棋盘上的棋子。

该系统允许无缝游戏，通过霍尔效应传感器检测玩家何时移动棋子，并向在线国际象棋服务器报告。类似地，当游戏状态被更新时，SCARA 手臂介入来移动反映远处玩家移动的相关棋子。

这是一个有趣的项目，并且肯定会点亮 Hackaday 社区中的许多 chessheads。我们以前也见过其他自动化的国际象棋，比如陷阱国际象棋，棋子可以随时从棋盘上突然掉下来。休息后的视频。

 [https://www.youtube.com/embed/X4pencncdEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/X4pencncdEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

