# 用于小型发动机的火花塞点火线圈

> 原文：<https://hackaday.com/2020/12/21/coil-on-plug-ignition-for-tiny-engines/>

火花塞是内燃机历史上的一项关键发明，它让燃烧更容易控制，让发动机比早期混乱的设计转得更快。世纪中期的汽车倾向于依靠带有分电器和线圈的点点火，然而更现代的设计是在每个单独的火花塞上放置一个线圈。[[罗杰·摩尔]决定在他的工作台上为一个小型发动机模型建造一个类似的装置。](https://www.youtube.com/watch?v=S1gIbXvlWjo&feature=youtu.be)

该设备由一个 Arduino、一个反激式变压器、少量 MOSFETs 和无源器件、一个 IGBT 和一个电容器组成。Arduino 通过 MOSFET 输出 PWM，该 MOSFET 通过变压器升压，然后给电容器充电。然后，电容器向安装在单缸发动机火花塞顶部的线圈放电，从而点燃火花。火花的定时由霍尔效应传感器读取放置在飞轮上的磁铁来确定。

后来的开发旨在进一步缩小系统，以适应[罗杰]计划进行的 V10 设计。在之前已经在小范围内完成了，我们希望看到另一个有太多汽缸的微型发动机。休息后的视频。

 [https://www.youtube.com/embed/S1gIbXvlWjo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/S1gIbXvlWjo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢安迪·皮尤的提示！]