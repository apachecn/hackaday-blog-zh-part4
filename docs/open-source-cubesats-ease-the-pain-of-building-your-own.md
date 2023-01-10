# 开源立方体减轻了构建自己的痛苦

> 原文：<https://hackaday.com/2021/01/28/open-source-cubesats-ease-the-pain-of-building-your-own/>

太空很难，尤其是如果你以前没做过。每年都有越来越多的立方体卫星由缺乏经验的小型团队发射，其中一些失败是因为遗漏了一些小而关键的硬件或软件问题。卡内基梅隆大学机器人探索实验室(REx)的研究人员已经从这些教训中吸取了一些教训，并创建了 [PyCubed](http://roboticexplorationlab.org/projects/pycubed.html) ，这是一个用于未来立方体卫星的开源硬件和软件框架。

大多数卫星，包括[立方体卫星](https://hackaday.com/2019/08/02/how-to-build-a-cubesat/)，都需要相同的基本构件。其中包括 ADCS(姿态确定和控制系统)，TT & C(遥测、跟踪和命令)，C & DH(命令和数据处理)，以及 EPS(电力系统)。这些构建模块均集成到一个 PC/104 尺寸的 PCB 中。主微控制器是 ATSAMD51，也用于几个 Adafruit 开发板上，运行 Circuit Python。通信由 LoRa 无线电模块处理，还有一个第二无线电的未占用空间。LSM9DS1 IMU 和可选的 GPS 处理导航和姿态确定，flash 芯片和 micro SD 卡提供 RAM 和数据存储。EPS 包括一个能量采集器和电池充电器，电源监控器和常规，可以连接到外部锂离子电池和太阳能电池板。两个功率继电器和一系列连接到燃烧导线的 MOSFETs 用于部署立方体卫星及其天线。

在 PCB 上有用于特定任务的多达四个独特有效载荷的标准化足迹。硬件和软件记录在 [GitHub](https://github.com/pycubed) 上，包括测试和所有设计决策及其合理性的完整文档。PyCubed 还在 2019 年 AIAA/亚利桑那州立大学小型卫星会议上亮相[。该平台已经作为](https://digitalcommons.usu.edu/cgi/viewcontent.cgi?article=4364&context=smallsat) [Kicksat-2](https://hackaday.com/2019/06/25/the-future-of-space-is-tiny/) 任务的一部分进行了飞行测试，还将用于即将到来的 [V-R3X](https://www.nasa.gov/ames/v-r3x) 、 [Pandasat](https://pandasat.net/) 和 [Pycubed-1](https://www.nanosats.eu/sat/pycubed) 项目。

这不是我们看到的第一个[开源立方体卫星](https://hackaday.com/2017/04/19/flying-the-first-open-source-satellite/)，我们希望这些平台变得更加普遍。追踪一颗立方体卫星比把它送上太空要便宜得多，而且对 T2 来说只需要 25 美元。