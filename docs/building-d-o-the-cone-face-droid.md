# 建筑 D-O，圆脸机器人

> 原文：<https://hackaday.com/2020/05/17/building-d-o-the-cone-face-droid/>

对我们许多人来说，电影是项目灵感的巨大来源，而《星球大战》电影是一份不断送出的礼物。D-O 机器人的出现和天行者的崛起相当于一只被遗弃的小狗，在 3D 打印的帮助下，[马特·丹顿]让它变得栩栩如生。(视频，嵌在下面。)

D-O 实际上是一个两轮自平衡机器人，在主体的外边缘有两个薄驱动轮。一个宽的柔性轮胎覆盖了两个轮子之间的空间，其中容纳了电子设备，但实际上并没有形成驱动机构的一部分。主驱动电机是一对带编码器的齿轮 DC 电机，允许闭环控制至非常低的速度。该操作的大脑是一个 Arduino MKR-W1010，它由电机驱动器、屏蔽、IMU 屏蔽和原型屏蔽组成。[Matt]确实在电机驱动板上发现了一个设计错误，这导致主电源开关 MOSFET 因栅极电压过高而起火。幸运的是，他能够通过简单地移除熔断的 MOSFET 并用电线桥接连接来解决这个问题。

正面 D-O 非常有表现力，[马特]用四个伺服系统来控制它的运动，另外三个用来激活它后脑勺上的三个天线。让所有的机制平滑地移动，没有任何倾斜，需要几次迭代才能正确，最终结果看起来和移动起来都非常好。

[马特]自己参与了这部电影的制作，所以他以另一位多产的机器人制作人[【迈克尔·巴德利】](https://www.facebook.com/groups/2152999025028674)的设计为基础进行制作，以避免破坏他的 NDA。他在一系列视频中涵盖了整个开发和测试过程，并将在完成后发布[设计文件和指令](https://www.facebook.com/groups/DOBuilders/)。

 [https://www.youtube.com/embed/2cIdjQiS2ZE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2cIdjQiS2ZE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

