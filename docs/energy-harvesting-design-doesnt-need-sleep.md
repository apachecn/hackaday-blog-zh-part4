# 能量收集设计不需要睡眠

> 原文：<https://hackaday.com/2018/07/19/energy-harvesting-design-doesnt-need-sleep/>

当涉及到电能收集时，每一点电能都是宝贵的，使用这种设计通常意味着熟悉微控制器的低功耗技巧和睡眠模式。但在[bobricius]的[超低功耗能量采集器设计](https://hackaday.io/project/85457)中，附加的微控制器根本不需要担心管理电源，只要它能足够快地完成工作。

这个想法是用太阳能充满一个电容，然后打开微控制器，让它正常运行，直到电量耗尽。因此，微控制器的运行时间可能只有几十微秒，但如果有足够的时间来读取传感器和传输数据包，那就没问题了。在早期测试中，[bobricius]能够使用小型光电二极管阵列作为电源，每 30 分钟可靠地无线传输一次 16 位值。这是另一件有趣的事情。[bobricius]使用 BPW34 光电二极管阵列收集太阳能。数据表将它们描述为硅光电二极管，但它们可以有效地用作小型塑料封装的太阳能电池。它们很容易获得，并且可以以多种配置排列，同时也相当耐用。

给电容器充电，然后短时间运行负载是管理太阳能的最简单方法之一，它不需要不寻常的组件或奇特的充电控制器。只要负载不介意短暂的运行时间，它可以是一种有效的方法，甚至可以将室内灯变成一个象征性的免费电源。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)