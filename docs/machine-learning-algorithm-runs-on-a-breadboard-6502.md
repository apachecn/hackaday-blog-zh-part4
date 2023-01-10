# 机器学习算法在试验板 6502 上运行

> 原文：<https://hackaday.com/2020/04/22/machine-learning-algorithm-runs-on-a-breadboard-6502/>

当谈到机器学习算法时，人们的想法不会自然地流向 6502，这种处理器在 PC 革命的第一波中为一些机器提供了动力。人们肯定不会想到[手势识别运行在自制的 6502 机器](https://github.com/nickbild/vectron_ai)的试验板上，然而这正是【尼克·比尔德】已经完成的。

在任何人在评论中过于激动之前，我们意识到[Nick]的 Vectron 试验板计算机正在从其他更现代的机器中获得很多帮助。他有一对 Raspberry Pi 3s，一个用于捕捉和缩小 Pi 摄像头的图像，另一个与 Atari 2600 仿真器连接，并根据摄像头看到的手势发送按键来控制游戏。但是把手势转换成控制信号的逻辑都是 Vectron，并且使用了一个在 6502 汇编中执行的*k*-最近邻算法。五十个手势图像存储在 ROM 中，并作为四个已知手势类别的参考:上、下、左和右。当找到相机图像和手势类之间的匹配时，相应的按键被发送到游戏。下面的视频显示，整个事情反应相当迅速。

在我们关于[尼克]的[Vectron 试验板电脑](https://hackaday.com/2019/04/19/a-nearly-practical-6502-breadboard-computer/)的原始文章中，[汤姆·纳尔迪]说“你不会在上面玩*波斯王子*。”这可能是真的，但在 Vectron 上运行的机器学习系统也不算太差。

 [https://www.youtube.com/embed/HILEYKIFixw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HILEYKIFixw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

