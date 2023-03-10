# 机器人在球形轮子上向任何方向移动

> 原文：<https://hackaday.com/2021/05/29/robot-moves-in-any-direction-on-ball-wheels/>

向任何方向移动和原地转向的能力对于在室内围绕其他物体操作的机器人来说是一项有用的功能。[詹姆斯·布鲁顿]展示了一种可能的解决方案，它是一种机器人底盘，可以通过三个球形轮子向任何方向移动。

休息后的视频是这个系列的第二部分。[第一部分](https://hackaday.com/2021/05/20/3d-printing-omni-balls-for-robot-locomotion/)讲述了球轮本身，由一对可以独立旋转的半球组成，每个半球的中心有一个小滚子，一根从动轴穿过球体的中心。其中三个围绕机器人中心以 120°的间隔排列，主轴由齿轮传动的 DC 电机通过皮带驱动。为了直线运动，使用一些基本的三角学来计算每个车轮所需的相对速度。Arduino Mega 用于在接收来自无线控制器的输入时进行必要的计算。

动作非常流畅，我们很有兴趣看看它与[麦克纳姆](https://hackaday.com/2019/07/28/a-3d-printable-mecanum-wheeled-robot-platform/)和[全向轮](https://hackaday.com/2016/02/20/mdf-omniwheel-uses-no-metal-or-plastic/)相比如何。对于真正有用的机器人，这似乎是[詹姆士]'[的完美平台。他暗示将来可能会在上面装一个垃圾桶。我们希望看到一个自动垃圾捕捉机器人，类似于](https://hackaday.com/2020/11/12/really-useful-robot/)[【stufmade here】的机器人篮球架](https://hackaday.com/2020/09/09/third-times-a-charm-for-this-basketball-catching-robot/)。

 [https://www.youtube.com/embed/zKLMCO0-How?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zKLMCO0-How?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

