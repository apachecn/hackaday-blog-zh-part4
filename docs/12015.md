# 与 DobsonianDSC 一起在星空中寻找您的路

> 原文：<https://hackaday.com/2021/11/25/find-your-way-in-the-starry-skies-with-dobsoniandsc/>

使用望远镜的一个显而易见的问题是让前者指向你想要观察的天空的适当部分，或者当你发现一些有趣的东西并希望记录下确切的位置时，反之亦然。虽然所有这些都可以手动完成，但有些麻烦，自动化这个过程有很多好处。不幸的是，这些数字设置圈(DSC)功能即使作为附加功能也不便宜，这就是为什么[ Vladimir Atehortúa ]创建了 [DobsonianDSC](https://github.com/vlaate/DobsonianDSC) 作为一种低成本的 DIY 解决方案。

顾名思义，这个项目是基于一个多布森式望远镜:牛顿管与简单的 altazimuth 基地。除了机械结构之外，该系统使用一个 ESP32 作为其控制器以及两个旋转编码器，简单的电路详见[构建指南](https://github.com/vlaate/DobsonianDSC/blob/master/docs/Solderless.md)。ESP32 的固件是用 Arduino C 方言编写的，同时还提供了一个关于[用 Arduino IDE 刷新 ESP32](https://github.com/vlaate/DobsonianDSC/blob/master/docs/UploadConfigure.md) 并将其连接到 WLAN 的指南。

设置完成后，最终的望远镜系统可以通过 WiFi 或蓝牙从支持“基本编码系统”的现有应用程序(如 SkySafari)中使用。需要进行初始校准，但之后你应该有一个与 SkySafari 或类似工具协同工作的望远镜，以自动化天文学的这一乏味部分。

显然，这不是一个现成的安装系统，因为每个望远镜的形状和大小都不同，但也提供了[安装解决方案](https://www.cloudynights.com/topic/772803-how-to-attach-altitude-encoders-to-dobsonians/)的灵感。