# 高格调的平衡球平台

> 原文：<https://hackaday.com/2019/02/02/high-style-ball-balancing-platform/>

如果宜家制造了[球平衡 PID 机器人](https://www.instructables.com/id/Ball-Balancing-PID-System/)，它们可能看起来就像这个。

这种[Johan Link]构建不仅仅是关于风格。深入了解一下，你会发现这并不是你所期望的标准、现成的微控制器开发板。相反，[Johan]用 ATmega32 设计并建造了自己的电路板，来运行控制平台的三个伺服系统。整个设备由十几个 3D 打印的部件组成，这些部件互锁形成底座、平台和 USB 网络摄像头的外壳，USB 网络摄像头位于铝管上。从这个有利位置，用 OpenCV 分析摄像机的图像，并定位球的中心。PID 回路控制三个伺服系统，使球在平台上居中，或者通过在受控的圆圈内移动球来使球稍微眼花缭乱。这是一个很好的构建，下面的视频展示了它的运行。

我们以前见过一些平衡平台，但很少有这种风格的。这个 Stewart 平台接近了，这个杂耍平台[通过音频反馈关闭控制回路](https://hackaday.com/2018/07/25/juggling-machine-listens-to-the-bounce-to-keep-ball-in-the-air/)获得了额外的分数。当然，还有杂耍。

 [https://www.youtube.com/embed/57DbEEBF7sE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/57DbEEBF7sE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

