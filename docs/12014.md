# 用软件无线电分析 Starlink 卫星下行链路通信

> 原文：<https://hackaday.com/2021/11/26/analyzing-starlink-satellite-downlink-communications-with-software-defined-radio/>

通常，仅仅是好奇心就足以做某事。这也是人们试图分析 SpaceX 与其基于 Ku 波段的 Starlink 卫星使用的通信设置和协议的情况。克里斯蒂安·哈恩(Christian Hahn)就是其中之一，他最近在 Reddit 上[向 *r/StarlinkEngineering* 发布了一些早期发现](https://www.reddit.com/r/StarlinkEngineering/comments/qwm1v5/observations_of_starlink_satellite_to_user/)。一些捕获的数据似乎包括卫星 ID 系统，地面用户站可能会使用该系统来跟踪头顶的 Starlink 卫星。

对于捕获本身，[Christian]正在使用一个二手盘子进行捕获，并使用基于 KC705 FPGA 的硬件 DIY SDR(这可能是作为加密挖掘硬件开始的),以及这种捕获的常见过滤器和其他常见组件。即使在这个早期阶段，Starlink 协议的一些特征看起来也很明显，例如信道的划分和保护期的使用。没有什么太惊天动地的，但作为一个有趣的 SDR 爱好，它肯定会检查所有的框。

[Christian]还宣布，他将在某个时候建立一个网站，并发布研究结果和代码，这将使 Starlink 信号分析对任何拥有现成 SDR 接收器的人来说都很容易。