# 迷你猎鹰 9 号使用美国宇航局的软件

> 原文：<https://hackaday.com/2022/07/26/mini-falcon-9-uses-nasa-software/>

[T-Zero Systems]已经为他的猎鹰 9 号模型火箭工作了一段时间。这是一个令人印象深刻的模型，配有推力矢量，遵循预定飞行计划的微控制器，工作发射台，甚至尝试垂直着陆的腿。然而，在他的模型的第一次测试中，他写的控制系统软件有一些问题，所以他带着从航天飞机借用软件的新系统“T2”回来了。

首先要解决的问题是万向节锁，这是一个在飞行过程中两个旋转轴对齐时出现的问题，导致运动不稳定。这是特别困难的，因为这个模型没有控制滚转的能力。使用四元数而不是欧拉角来解决这个问题涉及到大量的数学，由为航天飞机开发的库提供，但由于额外的效率改进，新软件的运行速度比以前快得多。不幸的是，新软件有一个阻止降落伞打开的错误，直到发射后才被发现。

在这个构建的幕后也有很多事情在进行，比如用于测试控制系统的测试火箭发动机，它实际上是两个反向旋转的螺旋桨，可以用来模拟发动机的推力，而不用实际点燃任何东西。还有一个[单独的视频](https://www.youtube.com/watch?v=VswtDcRY3UY)描述了一种测试方法，该方法使用之前发布的数据来验证新硬件。而且，如果你想让你的火箭模型朝着不同的方向发展，你也可以自己制造燃料。

 [https://www.youtube.com/embed/EHfsZGN3cYo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EHfsZGN3cYo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

