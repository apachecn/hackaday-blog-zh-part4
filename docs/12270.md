# OpenCV 知道你的手在哪里

> 原文：<https://hackaday.com/2021/12/23/opencv-knows-where-your-hand-is/>

我们不得不说，[穆尔塔扎]在他的最新视频中的示例游戏并不令人兴奋。然而，他使用的 OpenCV 技术追踪一只手并确定它与单个相机的距离是非常有趣的。演示在屏幕上显示一个随机按钮，你必须用手按下按钮，然后按钮移动，这样你就可以再试一次。手动测量似乎精确到几厘米，这对于许多应用来说已经足够好了。

Python 代码实际上非常简单。本质上，该软件跟踪你的手，并通过估计它的相对大小来确定它有多远。当然，你的手也可能会转动，而且[Murtaza]一步一步地处理所有情况。如果我们想知道距离，我们可能会求助于超声波或飞行时间传感器。问题是，那些传感器不能把你的手和碰巧在它前面的任何东西区分开来。使用单个摄像头来跟踪和定位是非常令人印象深刻的。

如果你以前没用过 OpenCV，频道有很多教程，都值得一看。计算机视觉是一项伟大的技术，在某些应用中可以取代很多东西。[比如 GPS](https://hackaday.com/2021/11/03/autonomous-drone-dodges-obstacles-without-gps/) 。或者，明年万圣节试试这个[更恐怖的追踪应用](https://hackaday.com/2021/10/30/skeleton-watches-you-intensely-because-its-halloween-okay/)。

 [https://www.youtube.com/embed/NGQgRH2_kq8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NGQgRH2_kq8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

