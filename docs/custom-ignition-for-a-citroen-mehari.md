# 雪铁龙 Mehari 的定制点火装置

> 原文：<https://hackaday.com/2021/02/05/custom-ignition-for-a-citroen-mehari/>

20 世纪见证了大量廉价、实用的车辆进入市场。像 Mini 和最初的 Jeep 这样的汽车提供了低成本、无装饰的驾驶。然而，它们显然也是低技术含量的，远不如现代汽车可靠。雪铁龙 Mehari 恰好属于这一类，当[FVFILIPPETTI]厌倦了不可靠的点式点火系统时，[他决定打造一款更现代的替代车型。](https://fvfilippetti.blogspot.com/2021/01/electronic-ignition-for-50-years-old.html)

该系统基于 ATmega328，这种古老的芯片很多人都熟悉，因为它在 Arduino Uno 中扮演了主角。该芯片通过安装在飞轮上的磁铁和霍尔效应传感器来跟踪发动机位置，通过光耦合器来避免火花系统的讨厌的高压尖峰干扰微控制器。然后，芯片给点火线圈充电，并在必要的时候点火，点燃空气燃料混合物。

老实说，与更现代的解决方案相比，老派的机械点火系统非常糟糕。这个版本给了[FVFILIPPETTI]一个更可靠的乘坐体验，我们确信这是非常令人满意的。如果所有这些黑客行为让你渴望拥有一个自己的汽车项目，那就看看我们的入门读物[如何进入汽车吧！](https://hackaday.com/2019/12/02/how-to-get-into-cars-choosing-your-first-project-car/)