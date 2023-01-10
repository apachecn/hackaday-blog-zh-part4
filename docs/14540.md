# 利用霍尔效应传感器进行 2D 和 3D 跟踪

> 原文：<https://hackaday.com/2022/08/19/tracing-in-2d-and-3d-with-hall-effect-sensors/>

受电弓曾被用作一系列任务的简单机械装置，包括复制简单的线条画。[Tim]决定做一个现代的电子版本[来代替 g 代码。](https://www.instructables.com/Tims-Electronic-Pantograph-2D/)

该设计依赖于 3D 打印的受电弓组件，安装在电路板上作为基座。一对霍尔效应传感器安装在受电弓上，与一系列钕磁铁一起，可以用来测量受电弓关节的角度。霍尔传感器由 Arduino Nano 读取，Arduino Nano 计算受电弓头运动的角度，并将其记录为 g 代码。这可以简单地显示在附加的 LCD 显示器上，或者卸载到计算机上存储。

[Tim]在早期的一篇文章中解释了这项工作背后的基本理论，他用同样的技术制作了一套电子分频器。他也没有就此止步。他还建造了一个更复杂的 3D 版本，他称之为电子点制图仪，可以通过一个 [3D 功能的缩放器](https://www.instructables.com/Tims-Electronic-Point-Mapper-3D/)机制来生成点云。

这是一个学习几何的好方法，如果你在描摹 2D 的画或者测量三维物体的时候会很有用。

 [https://www.youtube.com/embed/25-7GnLkfDI?feature=oembed&autoplay=1&version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/25-7GnLkfDI?feature=oembed&autoplay=1&version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

