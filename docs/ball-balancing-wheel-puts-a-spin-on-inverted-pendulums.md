# 球形平衡轮使倒立摆旋转

> 原文：<https://hackaday.com/2021/07/20/ball-balancing-wheel-puts-a-spin-on-inverted-pendulums/>

如果你深入到控制理论的领域，你无疑会遇到倒立摆问题。这些年来，这些平衡行为已经出现了许多变体，但仅仅因为以前有人做过，并不意味着没有空间来做新的事情。在这里，[大卫·冈萨雷斯]提出了这个经典问题，并给了它一个原创的旋转——字面上——其中的[平衡行为现在是一个在旋转的轮子](https://youtu.be/cWkFL8DlaAM)上不稳定平衡的球。(视频，嵌在下面。)再加上一点计算机视觉传感技术、一点无刷电机控制技术、一点数学知识，你就拥有了一个闭环系统，这个系统一定会吸引很多人的眼球。

[David 的]实现是经典控制理论与一些现代电子技术的健康结合。从理论上来说，有一个状态空间控制器来驱动球的角度和角速度为零。“状态”是四个术语的组合:球的角度、球的角速度、轮的角度和轮的角速度。[David]对每一项进行加权，并将它们加在一起，以创建一个输入值来调整驱动轮子的电机速度并平衡球。

从电子箱中，[大卫]选择了运行 Arduino 的 ESP32，运行[simple foc](https://simplefoc.com/)的定制[Janus 无刷电机控制器](https://github.com/byDagor/Janus-Controller)，以及运行 MicroPython 的带有附加摄像头的[Maix Bit](https://www.seeedstudio.com/Sipeed-MAix-BiT-for-RISC-V-AI-IoT-p-2872.html)微控制器来计算球的角度。最后，如果你想深入了解源代码，[David]已经在 Github 上发布了固件。

我们喜欢看到人们将一些控制理论融入到熟悉的电子产品中。随着精密传感器和电机控制器的不断改进，我们很高兴看到项目的前景再次发生变化。渴望更多的人关闭不稳定系统的循环？只需看看[u factory]的[滚珠平衡机器人](https://hackaday.com/2013/10/24/building-a-ball-balancing-robot/)和[Gear Down for What][两轮调速器](https://hackaday.com/2019/05/16/this-two-wheeled-rc-car-is-rather-quick/)。

 [https://www.youtube.com/embed/cWkFL8DlaAM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cWkFL8DlaAM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

