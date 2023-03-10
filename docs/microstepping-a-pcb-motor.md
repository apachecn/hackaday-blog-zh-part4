# PCB 电机的微步进

> 原文：<https://hackaday.com/2020/12/11/microstepping-a-pcb-motor/>

在过去的两年里，[Carl Bujega]因其 PCB 电机设计而声名鹊起。他最近的冒险是通过添加带有微步的位置控制将它变成一个[步进电机。](https://www.youtube.com/watch?v=OzqSzFZa2DY&)

我们大多数人知道的 NEMA 步进电机是同步步进电机，而[卡尔]的设计是永磁设计。它在定子上使用四个线圈，在转子/表盘上使用两个永久磁铁。通过用步进驱动器(微步进)改变通过四个极中的每一个的电流，转子的位置理论上应该可以以良好的分辨率被控制。不幸的是，这说起来容易做起来难。他实现了位置控制，但它在某些位置不停地跳步。

电机和控制器由单个柔性 PCB 组成，以减少层间距并增加线圈的磁场强度。然而，这产生了其他问题，因为电机轴没有一个牢固的安装点，并且当定子线圈通电时 PCB 弯曲。焊接控制器也是一个问题，因为通孔接头很容易撕裂，PCB 在热板上回流时会膨胀，有一次甚至会弹出元件。[Carl]最终将其中一个 PCB 电机安装在一个 3D 打印框架内，以严格限制所有电机组件，但它仍然存在步骤遗漏的问题。有什么解决问题的建议吗？把它们放在下面的评论里。

像他的其他 PCB 电机一样，扭矩很低，但应该适合仪表或时钟。带有集成电机的 PCB 时钟挂在车间的墙上会很酷。

使用的 TMC2300 步进驱动器[Carl]属于为 3D 打印机启用[静音步进](https://hackaday.com/2015/01/24/new-part-day-silent-stepper-motors/)的同一系列驱动器。我们已经报道了一些[卡尔]的 PCB 致动器冒险，从他的[原始设计](https://hackaday.com/2018/01/24/this-tiny-motor-is-built-into-a-pcb/)到[线性致动器](https://hackaday.com/2018/06/11/pcbs-as-linear-motors/)和[柔性视点显示器](https://hackaday.com/2019/07/09/flexled-is-a-unique-take-on-persistence-of-vision/)。

 [https://www.youtube.com/embed/OzqSzFZa2DY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OzqSzFZa2DY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

