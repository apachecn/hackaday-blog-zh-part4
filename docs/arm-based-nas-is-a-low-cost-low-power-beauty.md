# 基于 ARM 的 NAS 是一种低成本、低功耗的美

> 原文：<https://hackaday.com/2018/09/18/arm-based-nas-is-a-low-cost-low-power-beauty/>

NAS 对家庭网络来说总是一个方便的补充，但是它们可能有点贵。 [[Blake Burkhart]决定创建自己的](http://bburky.com/NAS/)，优先考虑预算和低功耗因素，次要目标是生产一些路由器和物联网功能。

香蕉 Pi R2 是满足这些要求的一个好选择，它是一个基于路由器的开发板，还支持双 SATA 连接器和千兆以太网。[Blake]对这个特殊 SBC 的性能有一些遗憾，但它在完全作为 NAS 运行时表现不错。

该设备的机箱是一个三托架热插拔硬盘模块，其中一个托架已被拆除，用于 Banana Pi。这是一个简单的想法，优雅地执行，看起来很棒。为了访问香蕉码头的端口，定制的丙烯酸侧板被激光切割，这也允许 led 发光——这是任何 DIY 服务器/计算机构建的必备条件。当将这个面板安装到现有的外壳上时，[Blake]不愿意冒险敲击易碎的丙烯酸树脂，而是选择用一个预燃的螺钉将螺纹熔化到塑料中。我们发现，如果你慢慢来，敲击丙烯酸通常是没问题的，但是热敲击听起来确实很有趣。

热插拔盘柜中内置的 12 V 风扇噪音太大，而且尺寸不标准，连接器也不标准。此外，只要风扇断开并检测到 0 RPM，就会触发蜂鸣器警报。[Blake]的解决方案是将连接器的电源引脚重新连接到 5 V 电源轨上；他发现在 5 V 下运行风扇会产生更安静的性能，同时保持硬盘足够冷。

我们发现，当谈到 DIY 网络设备和路由器时，有两种方法。要么创建完全符合您需求的定制解决方案，如[这款完美的家用路由器](https://hackaday.com/2018/04/12/building-the-perfect-home-router/)，要么解决您当前的设备，然后[开发一些技术来为您自动重启](https://hackaday.com/2018/01/31/router-rebooter-eliminates-hassles/)。