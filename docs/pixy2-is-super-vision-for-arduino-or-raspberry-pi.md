# Pixy2 是 Arduino 或 Raspberry Pi 的超级视觉

> 原文：<https://hackaday.com/2018/11/09/pixy2-is-super-vision-for-arduino-or-raspberry-pi/>

一个带摄像头的树莓派已经不是什么新鲜事了。但是 Pixy2 相机可以与各种微控制器接口，并且具有足够的智能来检测物体，跟随线条，甚至在没有主机帮助的情况下读取条形码。[DroneBot Workshop]对设备进行了[审查，他对相机非常感兴趣。你可以看下面的视频。](https://dronebotworkshop.com/pixy2-camera/)

当你看视频的时候，你可能会想这个相机要花多少钱。结果是大约 60 美元，这并不便宜，但就其提供的功能而言，也不算多。该相机可以检测线条、交叉点和条形码，以及您想要训练它识别的任何对象。该相机还拥有自己的光源和双伺服电机驱动装置，用于云台安装。

您可以通过 USB、串行、SPI 或 I2C 进行连接。在内部，相机以每秒 60 帧的速度处理，它可以在内部记住七个签名。有一个基于 PC 的配置程序可以在 Windows、Mac 或 Linux 上运行。你甚至可以用这个程序在相机与另一个像 Arduino 这样的微控制器对话时监视相机。

这款相机不是用来拍摄清晰照片或视频的，但它是为寻找东西而优化的，而不是为了图片质量。高质量的帧需要更多的处理能力，所以这是一个合理的交易。相机确实需要训练来根据颜色和形状找到物体。您可以使用基于 PC 的软件进行训练，但也可以使用依靠摄像机上按钮的独立程序进行训练。视频展示了这两种方法。

一旦经过训练，你甚至可以让 Arduino 寻找物体。有一个库，可以让你找到相机目前看到多少项目，并找出块是什么及其位置。很明显，识别很大程度上依赖于颜色，所以如果你的东西在不同的面上有不同的颜色或者有多种颜色，你可能需要进行实验。

当然，您可以使用一台装有 OpenCV 的足够大的计算机来获得这些结果，但是将所有这些都放在一个包中，并且可以从任何处理器上使用，对于正确类型的项目来说，可能是一个真正的游戏规则改变者。如果你想制造一个可以处理 5 路交叉路口和条形码命令的奇特循线机器人，这是显而易见的。

我们之前也见过类似 [OpenMV](https://hackaday.com/2018/09/23/the-tiniest-computer-vision-platform-just-got-better/) 的其他智能相机。谷歌也为 Pi 配备了一个[视觉处理器](https://hackaday.com/2017/12/17/googles-aiy-vision-kit-augments-pi-with-vision-processor/)。它有很多功能，但是假设您连接到一个 Pi。

 [https://www.youtube.com/embed/391dXDjqzXA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/391dXDjqzXA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

