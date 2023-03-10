# 蓝牙遥控汽车包在几个传感器

> 原文：<https://hackaday.com/2021/11/13/bluetooth-rc-car-packs-in-a-few-sensors/>

你有没有在房子里走来走去，急切地想知道周围的温度、湿度和气压？你有没有想过用一个小型遥控平台来捕捉这些数据？如果是这样，这个来自[tuenhidy]的项目将会是你一直在寻找的。

这个小遥控车是围绕一个可视的无线终端建造的。这是一个微控制器平台，带有一个已经连接的屏幕，以及内置的无线硬件和用于连接外部模块的 Grove 连接器。因此，汽车增加了 DHT11 温度和湿度传感器，以及使用 Grove 连接器的 BMP280 气压传感器。

驾驶汽车是通过与 Wio 终端通信的 Blynk 智能手机应用程序完成的。每个车轮上的小型 DC 电机通过一个 DFRobot 四电机护罩驱动。通过内置屏幕，遥控汽车可以显示从智能手机应用程序接收的命令，以及周围环境的温度、湿度和压力。

我们真的很喜欢简单的 PVC 底盘设计，这是一个简单的项目，展示了如何建立一个蓝牙控制的汽车。传感器收集的数据也可以在智能手机应用程序上看到，所以如果你需要在不离开沙发的情况下采样隔壁房间的情况，你可以很容易地做到这一点。

像这样的项目是熟悉电机和传感器工作的好方法。这也是简单机器人开发的一个很好的基础。我们以前也展示过来自[tuenhidy]的构建，我喜欢这个可以在瓶子上绘图的伟大的旋转绘图仪。休息后的视频。

 [https://www.youtube.com/embed/31elws65CzU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/31elws65CzU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

