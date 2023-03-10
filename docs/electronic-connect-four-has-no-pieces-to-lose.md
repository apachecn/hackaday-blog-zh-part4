# 电子连接四没有零件丢失

> 原文：<https://hackaday.com/2020/06/15/electronic-connect-four-has-no-pieces-to-lose/>

在软件中重新创建经典游戏是提高编码水平或从一开始就学习编码的好方法。但是如果你用硬件来做，你将获得比编码技能更多的东西。问问[Kelly]和[Jack]就知道了，当时他们为一个学校项目建造了这个基于 Arduino 的电子连接 4。

我们喜欢他们的解释设法简化游戏，并使它比原来的版本更有趣。所有玩家要做的就是打开它，并开始按下底部的街机按钮来选择他们想玩的那一栏。发光二极管从上到下发出动画，模拟塑料盘从电路板上落下。如果检测到一个胜利——同一颜色的四个连续走向任何方向——棋盘上填满获胜的颜色，游戏重新开始。

状态机目前对平局的情况不做任何事情，所以在侧面隐藏了一个重置按钮。正如[Kelly]和[Jack]在休息后的演示视频中解释的那样，这是他们希望在未来解决的问题，同时使选择您想要的任何战斗颜色成为可能。我们认为模仿光盘从底部溢出的重置动画也会很酷。

如果你以前从未在硬件上实现过一个游戏，这样的事情可能有点令人生畏。我们可以建议用 4×4 井字游戏来代替吗？

 [https://www.youtube.com/embed/iOVdD7y2BZc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iOVdD7y2BZc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

