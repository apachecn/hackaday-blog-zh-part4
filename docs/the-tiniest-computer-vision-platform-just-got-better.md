# 最小的计算机视觉平台刚刚变得更好

> 原文：<https://hackaday.com/2018/09/23/the-tiniest-computer-vision-platform-just-got-better/>

如果你相信广告文案，未来是一个充满由智能、神经网络和计算机视觉支持的摄像机的世界。尽管大肆宣传，但这实际上可能是真的:无人机正在获得智能摄像头，自动驾驶汽车装载了智能摄像头，无论如何，它都是一个很好的玩具。

[这就是这个 Kickstarter 如此令人兴奋的原因](https://www.kickstarter.com/projects/1798207217/openmv-cam-h7-machine-vision-w-micropython)。是的，这是一个相机模块，但它背后也有一些智能。OpenMV 是一款 MicroPython 驱动的机器视觉相机，它为您的项目提供了计算机视觉的力量，而无需携带笔记本电脑或 GPU。

OpenMV [实际上是从专注于一个简单想法的 Hackaday Prize entry](https://hackaday.com/2014/06/06/thp-entry-openmv/) 开始的。到处都有便宜的相机模块*，*那么为什么不在相机上安装一个处理器来进行机载图像处理呢？OpenMV 的第一个版本可以以 25 fps 的速度进行人脸检测，以超过 30 fps 的速度进行颜色检测，并成为数百个不同机器人加载计算机视觉的基础。

这次的众筹活动是在融资最新版本的 OpenMV 相机，有很多变化。相机模块现在是可拆卸的，这意味着 OpenMV 现在除了通常的彩色/滚动快门传感器外，还支持全局快门和热视觉。由于这款相机有一个更快的微控制器，这个最新版本可以支持 80 fps 的多斑点颜色跟踪。随着 FLIR 轻子传感器的加入，这款相机可以进行热感应，[并且由于一个新的库](https://community.arm.com/processors/b/blog/posts/new-neural-network-kernels-boost-efficiency-in-microcontrollers-by-5x)，OpenMV 还可以在神经网络的帮助下进行数字检测。

我们已经看到了很多使用 OpenMV 摄像头的构建，现在已经到了没有这种硬件就无法参加自动驾驶汽车比赛的地步。这个新版本拥有所有的功能，这是我们见过的将计算机视觉添加到任何硬件项目中的最佳方式之一。