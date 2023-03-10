# 感觉显示了良好的物理设计的重要性

> 原文：<https://hackaday.com/2018/10/04/senseation-shows-the-importance-of-good-physical-design/>

传感器网络项目通常主要关注电子设计元素，例如传感器和网关的架构和无线传输方法。然而，同样重要的是物理和实用的设计元素，如安装、可用性和可维护性。[Mario Frei]的 [SENSEation 项目](https://hackaday.io/project/120280)是一个传感器网络，旨在用于各种建筑的室内，它展示了物理设计元素的深刻重要性，以便创建易于安装、易于维护和有效的硬件。项目日志对过去的版本进行了很好的概述，并分析了哪些版本做得好，哪些版本做得不好。

一个例子是传感器节点的电源。过去的设计使用墙壁适配器来提供稳定可靠的电源，但这样做有实际的考虑。电源适配器不仅意味着每个传感器都需要一定量的电缆管理，而且人们永远不知道在建筑物的某个地方安装节点时会发现什么；电源插座可能不在附近，或者它可能没有任何空闲的插座。[Mario]发现由于这些问题，每个节点的安装可能需要 45 分钟。解决方案是传感器节点改用电池供电。通过精心的电源管理，一个节点在需要充电之前可以运行近一年，移除任何电缆管理或电源适配器意味着安装时间平均只需七分钟。

这只是在现实世界中部署传感器网络时发现的实际问题的一个例子，以及一些深思熟虑的设计变化的积极影响。用于 SENSEation 的 [GitHub 库拥有重现模块化设计所需的所有细节，所以请查看一下。](https://github.com/architecture-building-systems/Wireless-Sensor-Network)

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)