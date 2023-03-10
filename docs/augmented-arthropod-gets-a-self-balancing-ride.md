# 增强节肢动物获得自我平衡乘坐

> 原文：<https://hackaday.com/2019/06/14/augmented-arthropod-gets-a-self-balancing-ride/>

有许多人觉得和昆虫在一起不舒服。这是可以理解的，而且随着技术给这些多足动物增加了可以四处漫游的身体，情况只会变得更糟。[tech_support]就是其中之一，它欢迎我们的新节肢动物霸主，[甚至为它们建造了一辆可爱的新座驾，供它们四处游玩。](https://www.instructables.com/id/Augmented-Arthropod-Self-Balancing-Mech/)

这种构建遵循了自平衡机器人的通常特征，有一些有趣的变化。有双刷电机驱动，一个 Arduino Uno 运行显示。然而，该装置采用了[博世 BNO055 绝对方位传感器](https://cdn-learn.adafruit.com/downloads/pdf/adafruit-bno055-absolute-orientation-sensor.pdf)，而不是更常见的行人 IMU。它将磁力计、陀螺仪和加速度计集成在一个芯片上，并在板上处理所有复杂的传感器融合数学运算。这允许它输出更简单和更容易使用的方向数据。

然而，真正的派对文章更加有趣。这种自动平衡器不是无线电控制或直线跟踪算法，而是拥有自己的昆虫导航。昆虫被放在一个小房间里，用超声波传感器来确定它的位置。然后，昆虫可以通过在这个房间周围移动来控制机器人的移动。该团队甚至开发了各种代码，用于拨打不同类型昆虫的传感器系统。

这不是我们第一次看到用机器人硬件增强的昆虫，我们怀疑这将是最后一次。如果你自己正在做一个疯狂的科学项目，[给我们写封短信](http://hackaday.com/submit-a-tip)。休息后的视频。

 [https://www.youtube.com/embed/esiqaSfpYD4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/esiqaSfpYD4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

