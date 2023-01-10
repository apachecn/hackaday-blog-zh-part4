# 光跟踪机器人依赖于 LDRs

> 原文：<https://hackaday.com/2020/10/08/light-tracking-robot-relies-on-ldrs/>

如今，当进行任何类型的光学跟踪时，我们的思维会立即转向复杂的解决方案。Raspberry Pis、高端相机和机器学习工具链都浮现在脑海中。当然，如果你的目标比较简单，你不必把问题复杂化。菲尔是一个光线跟踪机器人，他非常乐意用老方法来做这件事。

PHIL 由运行双伺服运动平台的 Arduino Uno 组成，为传感器头提供平移和倾斜功能。传感器头本身由一个 3D 打印的十字形截面护罩组成，护罩在各个部分安装了四个光敏电阻。遮光罩有助于阻挡光线进入斜角传感器，使直接暴露在光线下的传感器和黑暗面上的传感器之间有更大的差异。这产生了更强的差异信号，因此当 Arduino 读取传感器时，PHIL 应该将传感器头指向哪个方向以跟随光线就更清楚了。

建造者(Sean O'Donovan)指出，PHIL 的建造没有任何实际目的，只是一个很酷的项目。我们当然同意，重要的是要注意，在这样一个项目中获得的技能在以后总是会派上用场的。这种技术对于追踪太阳非常有用，例如。休息后的视频。

 [https://www.youtube.com/embed/suA05NZpNAM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/suA05NZpNAM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

