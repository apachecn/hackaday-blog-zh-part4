# 专用绘图仪致力于解决手机上的文字游戏

> 原文：<https://hackaday.com/2022/07/23/purpose-built-plotter-pitches-in-to-solve-wordblitz-on-your-phone/>

似乎大多数黑客从来没有玩过一个游戏，至少不知道如何作弊。这并不是说我们是一群不诚实的人，至少一般来说不是。更重要的是，大多数游戏对我们来说挑战性要小于如何对游戏机制进行逆向工程。我们不打算作弊；它就这样发生了。

或者至少这是看待智能手机游戏作弊的仁慈方式，比如这个自动单词搜索解谜软件。这款游戏名为 *Wordblitz* ，它基本上是经典*拼字游戏*的一个实现，并带有额外的功能来释放更多的多巴胺，让你继续玩下去。没有人会上当，[ghettobastler]使用激光切割机从 MDF 中快速制作了一个 X-Y 台架，添加了一个带有铝箔的棉签形式的触控笔，以及一个基于简单网络摄像头的视觉系统。机架的底座有一个电容板，以便手写笔可以操作电话，以及一个 ArUco 基准标记框架，以帮助定位电话。

Raspberry Pi 处理该过程的机器视觉部分，该部分使用 OpenCV 来估计手机的位置并提取当前的游戏区块。游戏字段中的单词由[犹太区]以前编写的求解器定位；然后，一个脚本将 g 代码输入绘图仪，以极快的速度啄出答案，至少比[佩吉·希尔]还快。请参见下面的视频，了解正在解决的示例游戏。

如果你选择这样做，有一个警告:[ghettobastler]的解谜算法是基于一部法语词典，所以你必须为其他语言重新教授它。但是不管它是什么语言，这让我们想起了一些我们最近看到的*单词*解算器。

 <https://hackaday.com/wp-content/uploads/2022/07/wordblitz_demo.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2022/07/wordblitz_demo.mp4](https://hackaday.com/wp-content/uploads/2022/07/wordblitz_demo.mp4)