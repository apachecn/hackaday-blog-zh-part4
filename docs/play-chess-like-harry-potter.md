# 像哈利·波特一样下棋

> 原文：<https://hackaday.com/2019/02/09/play-chess-like-harry-potter/>

如果你是一个哈利波特迷，你可能记得其中一部电影展示了一个刘易斯岛的国际象棋，它的棋子根据玩家的语音命令移动。这一壮举经常被黑客复制，[amoyag00]有一个版本，它集成了树莓 Pi、Arduino、Android 和 Stockfish 象棋引擎，如果你想自己玩的话。你可以在下面看到这个游戏的视频。

有趣的是，该系统使用 3D 打印软件 Marlin 来处理 Arduino 的运动。我们假设在一条路径上移动棋子和移动打印头没有太大区别。这无疑是 GCode 的一种新颖用法。

为了实现这一点，需要整合许多部分。Android 和 Pi 之间有蓝牙连接。我们至少看到了 Java、Python、C++的代码。我们很难过地看到，建造它的团队不能再修改它了，因为它是一个学校项目，零件已经被回收用于新的学生班级。另一方面，也许其他人会复制并进一步扩展它。

我们总是很惊讶我们没有看到更多的哈利波特随身用品。在今年的超级大会上有一根魔杖。我们也喜欢[疯眼汉穆迪](https://hackaday.com/2017/11/21/mad-eye-for-the-wifi/)。当然，还有其他的，但是没有你想象的那么多，因为这个系列很受欢迎。

 [https://www.youtube.com/embed/XP4GMycFWes?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XP4GMycFWes?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

