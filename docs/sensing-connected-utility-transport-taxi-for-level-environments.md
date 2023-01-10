# 适用于水平环境的传感、连接、公用事业运输出租车

> 原文：<https://hackaday.com/2019/11/09/sensing-connected-utility-transport-taxi-for-level-environments/>

如果这听起来有点拗口，那就称之为[斯卡托——德克萨斯 A & M 大学](https://mxet.github.io/SCUTTLE/)设计的开源移动机器人。斯卡托是一款低成本(不到 350 美元)的机器人，设计用于多学科工程技术(MXET)项目的教学，用于 MXET 300 移动机器人本科课程的实验室课程和学期项目。因为它是为学术目的而设计的，所以这个机器人有很好的文档记录，当你按照说明操作时，它很容易复制。事实上，该团队正在寻找其他人来构建 SCUTTLE，并给他们反馈以改进其设计。

SCUTTLE 网站上有大量视频，可以带你了解制造、电子设备设置、机器人组装、编程和机器人操作。它们旨在帮助学生在一个学期内制造和操作移动机器人。机器人所需的大部分机械和电子部件都是现成的，很容易获得，其余的定制部件可以很容易地 3D 打印出来。其模块化设计允许您自由尝试不同的选项、功能和升级。斯卡托足够强大，可以携带高达 9 公斤(20 磅)的有效载荷，允许添加额外的硬件。为了保持低成本和易于建造，机器人使用简单的双轮驱动系统，使用一对齿轮电机。这迫使机器人以一种“非完整”的方式从原点移动到目的地，以一系列的左/右转和向前移动，因此运动规划非常有趣。

“天窗”机器人是用运行在 Linux 下的 Python3 编程的，已经在 BeagleBone Blue 或 Raspberry Pi 上进行了测试。《天窗软件指南》是熟悉系统架构的好地方。

标准配置使用超声波传感器来避免碰撞，使用标准 USB 摄像头来观察，使用编码器连接到车轮驱动滑轮来确定相对于起点的位置。可以添加可选的 USB 激光雷达进行区域测绘。额外的有效载荷能力允许添加额外的传感器、致动器或电池组。

为了补充[网站](https://mxet.github.io/SCUTTLE/)上的信息，额外的资源被发布在 [GitHub](https://github.com/MXET/SCUTTLE) 、 [GrabCAD](https://grabcad.com/library/scuttle-robot-v2-1-1) 和 [YouTube](https://www.youtube.com/playlist?list=PLeVnRAuL1kMk5i01CC8kCIVRevEhVnU1J) 上。制造一个天窗机器人应该是 maker spaces 的一个伟大的团队项目，希望让黑客开始学习机器人技术。我们在过去已经报道了许多教育机器人项目，但是 skutor 真正闪耀的是它以低成本携带相当不错的有效载荷的能力。

 [https://www.youtube.com/embed/1VYjcl6etOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1VYjcl6etOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/zskXQ2lYKKc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zskXQ2lYKKc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

