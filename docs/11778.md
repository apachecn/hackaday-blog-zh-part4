# 这个机器人无法将视线从钱上移开

> 原文：<https://hackaday.com/2021/11/07/this-robot-cant-keep-its-eyes-off-the-money/>

有人说没有比万能的美元更有价值的财富了。(诺伯特·扎雷亚)喜欢 Youtube 视频上的另类摇滚配乐，喜欢迷恋金钱的机器人，所以着手打造后者。

这个项目基本上很简单。树莓 Pi 3B+配备了 Pi 摄像机，并设置为控制连接到简单的平移/倾斜组件的双伺服电机。Pi 在面部跟踪模式下运行 OpenCV。这使得机器人能够在其视野范围内追踪货币，因为绝大多数货币上都有某人的头像。OpenCV 用于检测钱在视野中的位置，并引导 Pi 的摄像头朝向现金。

这是一个巧妙的重新利用 OpenCV 的面部检测算法，这比训练自己的资金跟踪系统要快得多。然而，看起来机器人也可以追踪普通的人脸。也许它可以被优化来做一个颜色检查，这样只有灰度或绿色的脸会被机器人跟踪。

这个项目做了什么有用或重要的事情吗？可以说不是，但如果一个机器人能如此迷恋金钱，也许我们都能学到一些东西。或者，它可能只是[Norbert]学习编程和机电一体化项目的一个有用的项目。不管怎样，我们都喜欢。好奇者可以在 Github 上找到代码。

多年来，以这种方式使用 OpenCV 已经变得很普遍。然而，如果你想探测猫，也许可以考虑试试 Tensorflow。休息后的视频。

 [https://www.youtube.com/embed/tgW5lv0qEUE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tgW5lv0qEUE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

