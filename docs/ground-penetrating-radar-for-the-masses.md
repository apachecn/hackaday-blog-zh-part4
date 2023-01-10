# 面向大众的探地雷达

> 原文：<https://hackaday.com/2019/02/07/ground-penetrating-radar-for-the-masses/>

雷达是一种有用的工具，其常见用途有探测飞机和观察天气。它还有一些不太为人所知的应用，比如一种被称为探地雷达(GPR)的技术。尽管很难通过固体物体发送和接收无线电波，但有了合适的设备，建造一个在地下也能工作的雷达是可能的。

探地雷达通常用于探测地下设施，但也应用于其他领域，如考古学和地质学。对于这些领域的人来说，[在 2017 年波兰国家电信研究所会议(pdf 警告)](http://gpradar.eu/onewebmedia/TU1208_GPRforeducationaluse_November2017_FerraraChizhPietrelli.pdf?bcsi_scan_fd86d3dd427d821e=0&amp;bcsi_scan_filename=TU1208_GPRforeducationaluse_November2017_FerraraChizhPietrelli.pdf)上，一个较便宜的 GPR 是一个小组的优先选择。该演示详细介绍了如何以 600 欧元左右的价格构建一个 GPR，这比商业产品要便宜得多。

该演示首先强调探地雷达的基础知识，然后详细介绍发射电路，接收电路和 DC 电源的硬件材料清单。它还详细介绍了使电路正常运行所需的软件背后的理论，并提供了代码。处理是在 32 位 Mbed 平台上完成的，GPR 的其余部分也是用易于获得的组件构建的。

看到有用的硬件项目将传统上昂贵的设备的成本降低到普通人可以承受的程度总是好的。甚至传统的雷达系统现在也只需几百美元就能买到，我们甚至已经看到了 T2 其他探地雷达系统的尝试。

感谢[Stefan]的提示！