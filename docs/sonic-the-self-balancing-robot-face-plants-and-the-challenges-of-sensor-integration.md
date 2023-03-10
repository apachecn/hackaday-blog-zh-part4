# 自平衡机器人索尼克:面部植物和传感器集成的挑战

> 原文：<https://hackaday.com/2020/02/26/sonic-the-self-balancing-robot-face-plants-and-the-challenges-of-sensor-integration/>

看一个孩子学跑步是一件快乐的事情，但有时也是痛苦的经历。[詹姆斯·布鲁顿]令人印象深刻的自平衡机器人索尼克似乎也是如此，即使它有可弯曲的膝盖和力敏感的腿。

我们最近报道了该项目的机械部分，现在【詹姆斯】已经添加了电子设备，将它变成了一个真正令人印象深刻的工作机器人(休息后的视频)。做到这一点并不是没有挑战，但幸运的是，他与我们分享了经验，消灭了一切。这个机器人的膝盖由一对带滚珠丝杠的电机驱动，这种电机不能反向驱动。这意味着需要外部传感器来允许电机主动响应输入，在这种情况下，外部传感器是腿上的称重传感器和用于平衡的 MPU6050 IMU。主控板是 Teensy 3.6，NRF24 模块提供远程控制。

[James]希望机器人能够在转弯时倾斜并处理不平坦的表面(小坡道),而不会翻倒或摔倒。倾斜部分相当简单(对他来说)，但不平坦表面的传感器集成证明是一个真正的挑战，需要多次迭代才能工作。第一种方法是在倾斜运动的方向上移动机器人来吸收它，然后回到水平位置。然而，这可能会导致它在稍微大一点的斜坡上翻倒。当试图用一条腿在斜坡上保持机器人水平时，当它回到水平地面时，它会发生剧烈的左右摇摆。这是通过使用称重传感器来抑制运动而得到纠正的。

听起来这个机器人的工作还远远没有结束，因为[詹姆斯]正在使它成为各种想法的 R&D 平台。他的下一个计划是给它添加激光雷达，希望它能够读取地形，以便更好地做出反应和避免障碍。整个项目已经开放源代码，这将有望帮助更多的人来处理这样雄心勃勃的项目。

想用自平衡机器人把脚弄湿吗？看看这个使用 Arduino 和步进电机的简单设计。

 [https://www.youtube.com/embed/zCGipe45_kw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zCGipe45_kw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/5fiCC_Gt8Qk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5fiCC_Gt8Qk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/zlucjoYLGi8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zlucjoYLGi8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

