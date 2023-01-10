# 无人驾驶飞机在没有全球定位系统的情况下躲避障碍物

> 原文：<https://hackaday.com/2021/11/03/autonomous-drone-dodges-obstacles-without-gps/>

如果你是[尼克·雷姆]，你会想要一架[无人机，即使在低空有计划外障碍物阻挡的情况下，它也能规划自己的路线](https://www.youtube.com/watch?v=p8frNNYQNV4)。(视频，嵌在下面。)当然，您可以从头开始构建它。

为什么？获得一架可以在电池电量低、信号丢失或接到命令时飞行路径甚至回家的无人机是足够简单的。只要去你最喜欢的零售商，搜索“gps 无人机”,你就能以低得惊人的价格买到。这是可能的，因为 GPS 接收器已经变得便宜、小、轻且省电。虽然所有这些廉价的无人机都可以按照预定的路径飞行，但它们通常是飞越任何障碍物，而不是绕过障碍物。

[Nick Rehm]设想了一种四轴飞行器，它可以做启用 GPS 的无人机可以做的所有事情，*不使用*GPS 接收器。[Nick]通过使用类似于谷歌地图使用的算法来实现这一点，数据来自典型的 IMU、用于计算机视觉的摄像头、用于高度的激光雷达以及用于检测位置和移动的英特尔实感摄像头。一个 Raspberry Pi 4 运行机器人操作系统运行自主表演，一个 Teensy 负责飞行控制职责。

我们真正喜欢[尼克]的视频是他对复杂技术的清晰呈现，以及对一个耗费了无数时间、耐心和胶带的项目的巨大幽默感。

我们不禁想知道 DARPA 是否会允许[Nick]在地下挑战中驾驶他的无人机，比如 2020 年在一座未完工的核电站举办的挑战。

 [https://www.youtube.com/embed/p8frNNYQNV4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p8frNNYQNV4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

