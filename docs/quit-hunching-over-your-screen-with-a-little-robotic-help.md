# 在机器人的帮助下，不要再趴在屏幕上了

> 原文：<https://hackaday.com/2021/10/20/quit-hunching-over-your-screen-with-a-little-robotic-help/>

[诺伯特·扎雷亚]发现了一个我们很多人都患有的问题——长期不良姿势。经常可以看到电脑用户弓着背对着屏幕，这最终会导致背部问题。他提到，大多数姿势矫正设备都很无聊，所以对[诺伯特]来说，显而易见的解决方案是制造一个简单的机器人，友好地推你到正确的位置。

这个简单的基于 Arduino 的构建使用无处不在的 [MPU-6050](https://invensense.tdk.com/products/motion-tracking/6-axis/mpu-6050/) ，它提供 3 轴加速度和 3 轴陀螺仪数据，所有这些数据都在片上处理，因此它可以测量你要去哪里，你的方向以及你旋转的速度。这是通过 I ² C 总线进行通信的，因此接入 Arduino 或 Raspberry Pi 是一件简单的事情。有很多开源库可以使用这个非常普通的设备，这有助于减少那些不熟悉编程一个相当复杂的设备的人的学习曲线。

目前，他正在将传感器安装在自己的身体上，并对其进行硬连线，因此已经有了一些改进的余地。操作前提很简单，如果车身角度偏离垂直方向超过 55 度，移动伺服系统，将车身推回到正确的位置。

[项目 GitHub 有需要的](https://github.com/Norbert01x/Posture-Corrector-Robot-)代码，Hackaday.io 上的[项目页面显示了接线图。](https://hackaday.io/project/182117-posture-corrector-robot)

这些年来，我们已经看到了很多关于这个主题的项目，像这个[向你发送移动通知的项目](https://hackaday.com/2020/12/16/sit-up-straight-open-source-bluetooth-posture-sensing/)，[一个基于超声波测距仪的设备](https://hackaday.com/2016/03/11/posture-sensor-reminds-you-to-sit-up-straight/)，还有一个甚至使用[网络摄像头来监视你的项目](https://hackaday.com/2014/05/06/a-webcam-based-posture-sensor/)。这一个有愚蠢的因素，我们喜欢这一部分。请关注[诺伯特],我们确信会有更多的好消息出现！

 [https://www.youtube.com/embed/K1aP64ZNP6A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K1aP64ZNP6A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

