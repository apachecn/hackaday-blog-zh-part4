# 教导 DC 伺服电机像步进电机一样工作

> 原文：<https://hackaday.com/2022/01/01/teaching-a-dc-servo-motor-to-act-like-a-stepper/>

[Frank Herrmann]有一个有趣的想法，将一个[齿轮传动的 DC 电机变成一个伺服电机组件](https://hackaday.io/project/183287-xmoto-dc-as-servomotor)，但是有一个类似步进电机的接口。通过在电机主体后面堆叠一些小 PCB，可以将一个 DRV8837 DC 电机驱动器和一对霍尔效应传感器挤在第一个 PCB 层的[上，磁性编码器紧紧贴在它后面。PCB 边缘的引脚头连接到第二块 PCB](https://oshwlab.com/xpixer/i2c-motor-controller-small-chip_copy_copy_copy_copy_copy) 的[上，第二块 PCB 承载着基于廉价 STM32L432 的微控制器。第二个 PCB 也包含相关的 LDO 和调试 LED。这些器件共同提供了读取编码器、控制电机旋转和监听连接到运动控制器上游的“步进电机驱动器”接口引脚所需的一切。这个的 Arduino 源代码可以在](https://oshwlab.com/xpixer/i2c-motor-controller-small-chip_copy_copy_copy_copy_copy_copy)[项目 GitHub](https://github.com/xpix/ServoStrap/tree/master/STM32_XMoto) 中找到。

虽然[Frank]提到这种组件在重量和扭矩方面优于 NEMA 17 型步进电机，但我们没有看到精确度和可重复性方面的确切数据，而这对 3D 打印等精确操作很重要。

这个项目是一个更大目标的一部分，即围绕这些“DC 电机步进电机”制造一台完整的 3D 打印机，我们将饶有兴趣地观看。

当我们谈到 DC 汽车公司的闭环控制时，[这里有另一个尝试做同样的事情](https://hackaday.com/2015/01/20/closed-loop-control-for-3d-printers/)，没有集成。如果这些对你来说太小，那么你总是[重新利用一些挡风玻璃清洗电机](https://hackaday.com/2018/07/13/supersize-diy-r-c-servos-from-windscreen-wipers/)。

 [https://www.youtube.com/embed/0IbSE-sqBWQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=342&wmode=transparent](https://www.youtube.com/embed/0IbSE-sqBWQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=342&wmode=transparent)

