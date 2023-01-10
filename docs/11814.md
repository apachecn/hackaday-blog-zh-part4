# 用廉价飞行时间模块构建的刺猬姿态传感器

> 原文：<https://hackaday.com/2021/11/02/hedgehog-gesture-sensor-built-with-cheap-time-of-flight-modules/>

飞行时间传感器曾经是昂贵的，能够测量光子本身的传播时间，并经常用于跟踪目的。然而，这项技术现在更便宜了，因此[jean.perardel]已经使用 TOF 传感器来构建一个有用且负担得起的手势跟踪系统。

该系统依靠四个 VL53L1X 飞行时间传感器，这些传感器具有 16×16 扫描阵列，并通过 I2C 总线进行通信。控制表演的是 Arduino MKR1010，尽管该项目应该也可以用一系列其他微控制器来实现。

该设备内置在一个可爱的刺猬形状的因素，液晶显示屏充当脸。它显示面部表情，这些表情表明系统是如何解释和响应手势的。它赋予了这个项目很多个性，这使得使用这个系统更加有趣。该系统的手势可用于通过 USB 发送按键，控制继电器或伺服系统，甚至发射红外信号来控制电视和其他硬件。

它实际上似乎是一个有用的手势控制界面，可以成为工作站设置的有用部分。我们也看到了手势控制的其他用途，比如控制机器人手臂。休息后的视频。

 [https://www.youtube.com/embed/_aPQWkaN12I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_aPQWkaN12I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

