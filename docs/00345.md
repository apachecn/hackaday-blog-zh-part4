# 没有专有层的运动协处理器

> 原文：<https://hackaday.com/2018/08/18/a-motion-coprocessor-without-the-proprietary-layer/>

当你有一个复杂的任务会消耗你的微处理器的时间和能量时，把它卸载到另一个硬件上是有意义的。我们都习惯于我们的计算机使用的图形芯片组的形式——专门的处理器，其在特定任务中的计算能力很容易超过我们的主 CPU。这种任务卸载在微控制器层面也同样适用。一个例子是 EM 微电子 [EM7180](http://www.emmicroelectronic.com/products/sensor-fusion-sensor-interface/sensor-fusion/em7180sfp) 运动协处理器。它从一个三轴陀螺仪/加速度计和磁力计获取输入，在任何情况下都可以作为一个“一劳永逸”的组件。给定一个 EM7810，您的主机可以通过简单的命令确定其航向和速度，无需任何艰苦的工作。

[Kris Winer]使用 EM7810，但对其缺点感到沮丧，决定[创造一种更通用的替代产品](https://hackaday.io/project/160283-max32660-motion-co-processor)。结果是一个小 PCB 容纳了 Maxim[MAX32660](https://www.maximintegrated.com/en/products/microcontrollers/MAX32660.html)ARM Cortex M4F 微控制器和相关传感器，max 32660 增加的功率和集成的闪存轻松超越了 EM7810。

作为一个设计练习，这是一本有趣的读物，即使你并不需要。他的文章详细介绍了运动协处理器技术的现状，然后仔细研究了如何利用 OSH Park 等廉价的 PCB 制造公司来推动可能的极限——你可以将这种芯片作为晶片级封装(WLP)来获得，这绝对是禁区。尽管他选择了 TQFN-24，但结果是一个小小的电路板，我们很高兴地将它视为方寸项目回归的一个项目[！](https://hackaday.io/contest/160135-the-return-of-the-square-inch-project)

可能令人惊讶的是，像这样的项目很少进入我们的领域，作为一个社区，我们倾向于专注于让一个处理器做所有的艰苦工作。但是随着廉价而强大的设备的出现，也许这是一种我们应该重新考虑的方法。