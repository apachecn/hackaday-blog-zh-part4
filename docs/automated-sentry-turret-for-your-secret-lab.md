# 你的秘密实验室的自动岗哨塔

> 原文：<https://hackaday.com/2021/06/06/automated-sentry-turret-for-your-secret-lab/>

当您试图完成一些重要的黑客工作时，没有什么比入侵者未经允许反复出现更令人沮丧的了。[所有部件组合]为您提供解决方案，基于 [Kinect 的机器人哨兵炮塔](https://www.electromaker.io/project/view/kinect-based-sentry-turret)可以阻止他们。

该系统由一台连接到 PC 的微软 Kinect V2 组成，PC 运行一个应用程序来完成所有处理，并通过串行将目标信息输出到 Arduino。Arduino 控制一个简单的 2 轴伺服支架，上面绑着一个电动气枪。触发开关被一个继电器取代，也连接到 Arduino。

Kinect V2 配备了真正简化跟踪人体运动的 SDK，并以易于使用的格式输出数据。[所有部分组合]使用了 Unity 中的 SDK，这允许他选择要跟踪的身体部分。他添加了脚本来检测一些基本的手势，发出语音命令，并为 Arduino 生成串行命令。使用从 SDK 接收的目标的 XY 坐标以及 Kinect 和转台之间的已知距离，通过简单的几何计算伺服角度。当入侵者进入 Kinect 的视野时，它会立即瞄准入侵者的心脏，发出“举起手来！”命令，并告诉入侵者离开。如果入侵者不遵守，它会在开火前开始倒计时。[所有部件组合]还增加了一个秘密解除武装的手势(双手手枪)，它把炮塔变成了一个道歉的同志。它所需要的只是一个受门户启发的外壳。

这是一个有趣的项目，展示了 Kinect 如何使复杂的计算机视觉任务变得相对简单。不幸的是，V2 已经停产，取而代之的是更贵的、面向开发者的 Azure Kinect。我们已经报道了几个基于 Kinect 的项目，包括一个 [3D 房间扫描仪](https://hackaday.com/2015/12/10/3d-scanning-entire-rooms-with-a-kinect/)和一个[机器人篮球架](https://hackaday.com/2020/09/09/third-times-a-charm-for-this-basketball-catching-robot/)。

 [https://www.youtube.com/embed/e5JpQQOPFPk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e5JpQQOPFPk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

