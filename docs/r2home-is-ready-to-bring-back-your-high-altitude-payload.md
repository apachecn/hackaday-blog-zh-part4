# R2Home 准备好带回你的高空载荷了

> 原文：<https://hackaday.com/2022/08/01/r2home-is-ready-to-bring-back-your-high-altitude-payload/>

在高空气球飞行中，你受到风的支配，风可以将你的有效载荷移动数百公里，并将其存放在一些无法到达的地方。为了解决这个问题[【Yohan Hadji】创造了 R2Home](https://hackaday.io/project/176621-r2home) ，这是一个基于降落伞的自主回收系统，可以将有效载荷飞行到其滑翔范围内的任何指定着陆点。

我们第一次报道 R2Home 是在 2021 年初，当时他还处于早期的实验阶段，但是从那以后这个项目已经非常成熟了。它刚刚完成了它的[最长和最高的试飞](https://www.youtube.com/watch?v=NDLpS5nnJzU)。它携带一个额外的无线电探空仪有效载荷，从 3500 米的释放高度自主下降，在离发射点 5 米以内着陆。

![R2Home electronics with it's insulated enclosure](img/fc364370233f3bb69fc05c53145ea8ab.png)

R2Home electronics with its insulated enclosure

R2Home 可以使用各种可操纵的座舱盖飞行，甚至可以使用 DIY 冲压空气降落伞，如早期版本所示。【Yohan】目前使用的是 RC 滑翔伞的高性能机翼。

大量的努力投入到开发一个可靠的降落伞部署系统。主伞被小心地包装在一个定制的“Dbag”中，该 Dbag 连接到一个减速伞滑道上，以在自由落体过程中稳定系统，并在预设的高度展开主伞。这是通过伺服操作的释放机制来完成的，而转向是由一对用于遥控帆船的改良绞盘伺服系统来控制的。

所有的电子设备都安装在一堆圆形 3D 打印支架上，这些支架安装在管状外壳中，用螺纹杆栓接在一起。在一名设计专业学生的帮助下，[Yohan]还将简单的管状外壳升级为可锁定的泡沫绝缘设计，以帮助它应对高海拔地区的温度。

飞行主计算机是一个插入定制 PCB 的 Teensy 4.1，用于连接所有导航、通信和飞行系统。定制的基于 Arduino 的自动驾驶仪从 GPS 接收器接收输入，并将系统引导到所需的降落区，并在着陆前一直盘旋。

整个项目都有非常好的文档记录，所有的设计文件和代码都是开源的，可以在 Github 上找到[。](https://github.com/YohanHadji/R2Home)

 [https://www.youtube.com/embed/hcsJ6VtcOVQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hcsJ6VtcOVQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

