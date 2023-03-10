# 星际迷航水龙头控制器，第二次

> 原文：<https://hackaday.com/2021/11/18/star-trek-tap-controller-take-two/>

工程学学生和 DIY 爱好者[Xasin]认为控制各种家庭设备的通常方式，如手机应用程序和网络界面，太无聊了。相反，他开发了可穿戴的 Tap 界面，这是星际旅行通信徽章和移动全息发射器的结合。基本的想法是通过点击挂件来控制东西。但是自从两年前这个项目开始以来，事情变得有点失控。

![](img/d2e217ff50f9343607d551e6000e1ddc.png)

[Xasin]从 2019 年的 [Tap 版本 1](https://hackaday.io/project/161097-tap-to-control) 开始，学习了所有关于为 BLE 编码、制作 3D 打印外壳的知识，并最终解决了系统中的所有问题。Tap v1 使用电容触摸感应，但当前版本使用加速度计检测物理点击，也可以检测手势。一路上的功能蔓延带来了一个传感器阵列，一个情绪 LED 阵列，一个有机发光二极管屏幕和一个扬声器。整个系统由双核 ESP32 Pico MCU 驱动。[Xasin]已经在 GitHub 上发布了他的项目，如果你想自己探索这些特性的话。

![](img/a6ad09fe9f2e0036fb93c2d7d03386d6.png)

该项目只是部分启动和运行，因为由于全球零件短缺，一些关键部件不可用。但它很快就能控制智能家居设备，比如我们今年早些时候报道过的[Xasin]独立的 Dragon's Home 智能家居系统[。如果你想了解更多关于水龙头控制的一般知识，](https://hackaday.com/2021/08/16/voice-controlled-smart-home-from-the-foundation-up/)[查看 2018](https://hackaday.com/2018/08/21/turning-everything-into-a-tap-controller/) 的这篇文章。你可以在休息时间下面的短视频中看到 Tap 介绍自己和它的功能。

 [https://www.youtube.com/embed/_JhhvkacBVM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_JhhvkacBVM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

