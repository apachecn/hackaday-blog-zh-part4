# 用围棋棋盘音序器制作音乐

> 原文：<https://hackaday.com/2020/10/05/go-board-step-sequencer-lets-go-make-some-music/>

想知道你最喜欢的桌游听起来像什么吗？我们也没有。谢天谢地[Sara Adkins]做到了，并创建了一个名为 Let's Go 的[步序器，它使用经典的棋盘游戏 Go 作为输入。](http://www.saraadkins.com/portfolio.html#letsgo)

在围棋游戏中，两名玩家在格子上放置黑白代币，争夺棋盘的控制权。随着游戏的进行，游戏棋子的配置变得更加复杂，并且巧合地开始类似康威的《生命的游戏》(或者一个怪异的二维码)。萨拉在不断演变的圆圈排列中看到了音乐，并将古老的棋盘游戏转变为现代乐器，这样其他人也能听到。

对于一个观察者来说，改编的版本看起来与 2500 年前在中国播放的版本几乎没有什么区别——当然，除了头顶上的网络摄像头和旁边的笔记本电脑。笔记本电脑使用 OpenCV 来数字化电路板布局。它通过[开放式声音控制(OSC)](http://opensoundcontrol.org/) 将信息输入流行音乐创作软件 [Max MSP](https://cycling74.com/) (尽管开源版本可能会在[纯数据](https://puredata.info/)中实现)，在那里它被用来控制步进音序器。棋盘上的每一行代表一种乐器的声音(白色的曲子是旋律，黑色的曲子是打击)，每一列对应一个节拍。

每一个新的游戏都是一首新的音乐，从简单开始，逐渐变得复杂。音乐随着棋盘而发展，并为玩家与游戏的互动增加了新的维度。如果你想自己尝试一下，[Sara]在她的网站上有这个项目的完整文档，所有代码都可以在[GitHub](https://github.com/Satrat/lets-go)上找到。现在我们只是想知道其他游戏听起来像什么— [【廷卡坦克】已经回答了国际象棋](https://hackaday.com/2012/04/18/chess-board-step-sequencer/)的问题，但是卡坦的定居者呢？

 [https://www.youtube.com/embed/9pOlywOpmJY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9pOlywOpmJY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

