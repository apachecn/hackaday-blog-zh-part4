# 智能立体摄像机使用索尼无线摄像机模块

> 原文：<https://hackaday.com/2022/04/30/clever-stereo-camera-uses-sony-wireless-camera-modules/>

立体摄影相机很难找到，所以我们非常感谢[DragonSkyRunner]分享了他们制作的一个非常高质量的例子。立体摄像机有两个分开的镜头和传感器，它们相距固定的距离，这样当用每只眼睛分别观看两个结果图像时，就有 3D 效果。这款相机采用了两台独立的索尼相机，并将它们安装在一个精心设计的木制底盘上，但这种简单的描述隐藏了一个更加有趣和复杂的现实。

索尼曾经用 QX 系列测试过摄影技术——一对不寻常的无反光镜相机模型，只采用了传感器和镜头的形式。与智能手机的无线连接允许显示和数据传输。这个版本使用了其中的两个，一对运行 Android 的 Odroid C2s 代替了智能手机。它们的 HDMI 视频输出由一对连接到 Raspberry Pi 4 的 HDMI 捕获设备捕获，还有几个 Arduinos 模拟 Odroids 的鼠标输入。这有点像 Rube Goldberg 的设备，但它允许系统使用索尼的原始相机软件。一个特别巧妙的特点是，相机单元和显示器单元可以分开进行远程摄影，这使它成为一个非常多功能的相机。

很高兴看到专门为高质量摄影设计的立体摄影相机，我们之前看到的相机更接近机器视觉系统。