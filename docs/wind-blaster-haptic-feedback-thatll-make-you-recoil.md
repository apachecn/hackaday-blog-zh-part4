# 疾风枪:能让你退缩的触觉反馈

> 原文：<https://hackaday.com/2018/09/16/wind-blaster-haptic-feedback-thatll-make-you-recoil/>

虚拟世界的一大挑战是无论你身在何处都能获得触觉反馈。当你坐在椅子上时，这不是太大的问题，硬件可以连接到椅子或你附近的东西上，这就是所谓的接地力反馈。但是有了虚拟现实，我们已经习惯了至少在一个房间里走动。那么，你如何感受枪的后坐力、对盾牌的压力、剑划破空气的惯性，或者魔法剑发出闪电的脉动？

南韩 KAIST 大学[MAKinteract Lab]的一组研究人员已经开发出一种小型装置，可以绑在你的手腕上，提供所有这些类型的反馈。它被称为[风力推进器](http://seungwooje.com/wp-content/uploads/2018/05/wind_blaster.pdf)，由两个导管螺旋桨组成，可以提供高达 1.5 牛的力量。两个螺旋桨都安装在伺服系统上，在 IMU 的帮助下，螺旋桨可以根据需要调整方向。Arduino 进行 PWM 控制电机速度。

发射 VR 霰弹枪，螺旋桨在短短 250 毫秒内快速旋转至 33，000 RPM，让你的下臂快速向后拖曳，提供后座力枪的感觉。在空中挥舞一把虚拟现实剑，螺旋桨以 33，000 RPM 的速度旋转 400 毫秒，然后在 300 毫秒内线性减速直至停止。让螺旋桨相对于彼此异步移动会在你的手臂上产生旋转扭矩，为魔法闪电剑带来脉动感。连接的 PC 使用 Unity 游戏引擎运行游戏。与无人机一样，有大约 41 分贝的噪声，但用户的耳机将其屏蔽。请观看下面的视频。

在 Hackaday 上，我们已经介绍了一些不接地的触觉反馈系统。有一个[对光](https://hackaday.com/2014/12/18/touching-light-with-haptic-feedback/)做出反应，另一个[让你感受纹理](https://hackaday.com/2018/03/22/what-we-need-to-try-in-haptic-hacks/)，还有[一个在控制机器人手爪](https://hackaday.com/2016/06/29/wireless-robotic-gripper-with-haptic-feedback/)时获得反馈的手套。

 [https://www.youtube.com/embed/hCk0v8-pl20?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hCk0v8-pl20?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/FIdx4W9sazk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FIdx4W9sazk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

