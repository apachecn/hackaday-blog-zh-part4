# 开源自动驾驶智能手机机器人

> 原文：<https://hackaday.com/2020/11/06/open-source-self-driving-smartphone-robot/>

我们的智能手机本身就是非常强大的计算机，但我们并不经常看到它们被直接集成到项目中。英特尔智能系统实验室已经通过发布基于开源智能手机的自动驾驶机器人 [OpenBot](https://www.openbot.org/) 做到了这一点。

大多数神奇的事情都发生在智能手机上，智能手机运行一个基于 TensorFlow Lite 构建的应用程序，集成了智能手机上的摄像头和传感器阵列，以及机器人上的超声波传感器和车轮编码器的数据。机器人本身相对简单，有四个齿轮传动的 DC 电机，电机驱动器连接到 Arduino Nano，Arduino Nano 通过串行接口与 Android 手机连接。

由英特尔 ISL 团队开发的应用程序预装了三种人工智能模型，可以进行人员跟随，或两种不同的自主导航模式。通过将蓝牙控制器连接到智能手机，并在收集数据的同时在您的特定环境中手动驾驶机器人，您可以训练一个定制的自动驾驶策略来适应您的环境。

这看起来是一个用小预算体验自主机器人的绝佳方式，同时也是更苛刻应用的可行基础。我们只见过少数基于智能手机的机器人，如 [DriveMyPhone](https://hackaday.com/2016/05/17/smartphone-based-robotic-rover-project-goes-open-source/) 和 [SmartiPresense](https://hackaday.com/2020/08/06/telepresence-robot-navigates-upgrades/) ，它们没有人工智能功能，但旨在用于远程呈现应用。我们一直想知道[为什么我们没有看到更多使用手机的项目](https://hackaday.com/2018/10/18/ask-hackaday-why-arent-we-hacking-cellphones/)，所以我们欢迎这个例子。

 [https://www.youtube.com/embed/qc8hFLyWDOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qc8hFLyWDOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

