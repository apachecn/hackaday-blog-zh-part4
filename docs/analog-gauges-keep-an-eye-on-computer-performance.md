# 模拟仪表关注计算机性能

> 原文：<https://hackaday.com/2019/09/19/analog-gauges-keep-an-eye-on-computer-performance/>

密切关注计算机的资源利用率会很有用，尤其是当您经常执行计算密集型任务时。虽然这完全可以通过软件工具来实现，但创建一个专用的硬件监视器也很酷。马赛丽·卡拉诺维奇就是这么做的，用的是一套老式的模拟仪表。

该建筑使用 STM32 微控制器通过 MCP4728 数模转换器驱动一系列四个检流计。关于 CPU、内存、网络和 GPU 利用率的数据由 Python 脚本收集，并通过 USB 串行连接发送。该数据驱动四通道 DAC，进而产生控制压力表指针位置的电压。从美学角度来看，该建筑有一些不错的设计，包括定制的仪表面和带有雅致哑光饰面的 3D 打印外壳。定制的 PCB 可以保持电子设备和线路的整洁。

[马赛丽]做了大量的工作来解释设备的基本理论，以及使用基于检流计的量规的实际考虑。这将是一个伟大的周末项目，任何人都想为他们的桌面钻机添加一些复古的魅力。还可以监控其他变量，如硬盘使用率或 CPU 温度。如果你把它集成到笔记本电脑中，会有额外的好处；举报热线很想知道。我们以前也见过[基于 LED 的监控系统。](https://hackaday.com/2011/10/04/pc-temperature-monitoring-system-lights-up-when-things-get-hot/)休息后的视频。

 [https://www.youtube.com/embed/rDg91r9Q68E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rDg91r9Q68E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

