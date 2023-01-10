# 用机器视觉为经典的 Atari 2600 游戏添加激光发射器

> 原文：<https://hackaday.com/2021/06/03/adding-a-laser-blaster-to-classic-atari-2600-games-with-machine-vision/>

还记得最初雅达利 2600 的手枪控制器吗？没有吗？也许那是因为它从未存在过。但是现在我们生活在未来，[在 2600](https://github.com/nickbild/laser_blaster) 的经典游戏中加入手枪实际上是可能的。

有可能，但并不容易。[Nick Bild]解决问题的方法基于机器视觉，使用 NVIDIA Xavier NX 运行 Atari 2600 仿真器。游戏被投影在墙上，同时一台摄像机监视着游戏场地。一把装有激光笔的玩具手枪向目标开火，而 OpenCV 则被用来寻找被激光击中的位置。一个 Python 程序将激光爆炸的坐标与游戏中的坐标进行匹配，然后发出一系列键盘命令来启动游戏中的爆炸装置。基本上，游戏是根据它在哪里看到激光来玩的。您可以在下面的视频中查看该系统。

[尼克图片]有一个繁忙的黑客周末。这是他发给我们的第三份项目报告，之前是他的大屏幕 ardu boy build T1 和 T2 的 C64 智能手表 T3。

 [https://www.youtube.com/embed/_1XSo25VdcU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_1XSo25VdcU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

