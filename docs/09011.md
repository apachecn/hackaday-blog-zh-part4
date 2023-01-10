# 用一个坏马达控制四轴飞行器

> 原文：<https://hackaday.com/2021/01/28/controlling-a-quadcopter-with-one-dead-motor/>

四轴飞行器拥有令人难以置信的飞行能力，但如果其中一个失去一个发动机，它就会像石头一样掉落。苏黎世大学机器人和感知小组的研究人员已经证明，不需要通过只使用三个马达来保持四轴飞行器飞行。

四轴飞行器通常只有三个发动机就有足够的推力保持在高空，但它会在偏航轴上不受控制地旋转。要让四轴飞行器停止旋转是不可能的，所以研究人员的重点是保持无人机在旋转时可控。为了实现这一点，需要精确的位置和运动估计，所以他们在船的底部安装了一对摄像机，用于视觉惯性里程计(VIO)。一个是普通的光学相机，另一个是事件相机，其像素可以独立地响应光线的变化。这意味着它具有更好的弱光性能，不会出现运动模糊。

来自摄像机的反馈由机载 Nvidia Jetson TX2 进行实时分析，以进行状态估计，然后与光学距离传感器和机载 IMU 一起使用，以保持受控飞行，如休息后的视频所示。[研究论文](http://rpg.ifi.uzh.ch/docs/RAL21_Sun.pdf)免费阅读，所有的[代码都可以在 GitHub](https://github.com/uzh-rpg/fault_tolerant_control) 上获得。

无人机控制方案的新发展总是令人着迷，比如这款[六轴直升机采用创新的电机](https://hackaday.com/2021/01/09/six-degrees-of-freedom-omnicopter-with-ardupilot/)布局来实现六个自由度，或者一款[传统直升机采用虚拟旋转斜盘](https://hackaday.com/2020/06/25/building-and-flying-a-helicopter-with-a-virtual-swashplate/)。

 [https://www.youtube.com/embed/Ww8u0KH7Ugs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ww8u0KH7Ugs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示！