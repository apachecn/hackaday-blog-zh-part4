# Moteus 开源 BLDC 控制器获得重大升级

> 原文：<https://hackaday.com/2022/07/04/moteus-open-source-bldc-controller-gets-major-upgrade/>

mjbots 机器人系统公司的[Josh Pieper]刚刚发布了他的 *moteus* 开源无刷 DC (BLDC)电机控制器的重大修订。此次更新增加了一个灵活的 I/O 子系统，大大扩展了控制器可以接受的反馈编码器和外设的种类。在休息时间下方的视频中，[Josh]介绍了 11 种不同的示例配置。如果你愿意，这些例子也会以[文章的形式出现在他的博客](https://jpieper.com/2022/06/30/flexible-i-o-worked-examples/)上。

![](img/30f7fc9f43fa34265eefc98fd0214012.png)

*moteus* 控制器最初是在【乔希】开发 [quad A0](https://hackaday.io/project/167845-mjbots-quad) 时出现的，这是一种开源的动态四足机器人，沿着麻省理工学院迷你猎豹或波士顿动力机器狗的路线，并不满意现有的控制器可以做到这一点。这是一款基于 STM32G4 的紧凑型 50 mm 方形电路板，集成了磁编码器，并接受外部传感器连接。利用基于寄存器的方案，通过 CAN-FD 与电路板接口。Python GUI 工具通过逻辑树结构提供基于名称的寄存器访问，以及用于诊断和配置任务的实时遥测绘图功能。

如果你在你的项目中使用 BLDC 汽车，一定要看看这个。即使你没有使用 *moteus* 控制器，【Josh】对各种编码器反馈技术的演示也是非常有趣和有教育意义的。整个项目是开源的，硬件和软件设计文件都可以在项目的 [GitHub 库](https://github.com/mjbots/moteus)上找到。对于一些用户来说，这可能是一个主要因素，考虑到最新的 ODrive BLDC 控制器产品[已经成为闭源](https://discourse.odriverobotics.com/t/customisation-of-new-odrive-generation/9340)。

我们在 2019 年写了关于 [mjbots quad A0，你可以在 Hackaday.io](https://hackaday.com/2019/10/03/amazing-open-source-quadruped-capable-of-dynamic-motion/) 上关注 [*moteus* 项目。我们还通过[Skyentific]比较三个流行的开源 BLCD 控制器发现了这个有趣的视频，包括 *moteus* (休息后的第二个视频)。如果你想深入了解 BLDC 汽车公司的磁场定向控制，还有我们去年讨论过的 SimpleFOC 项目。感谢[安卓德鲁]的提示。](https://hackaday.io/project/179234-moteus-brushless-controller)

 [https://www.youtube.com/embed/a3UA6yzzgkE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/a3UA6yzzgkE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/Wb1gsJ4K4pM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Wb1gsJ4K4pM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

