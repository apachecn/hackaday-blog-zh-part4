# 一个切面包皮、切胡萝卜的机器人

> 原文：<https://hackaday.com/2020/11/30/a-crust-cutting-carrot-chopping-robot/>

确实讨厌面包皮。请注意，不是自制面包的上面部分——只是商店买来的面包边缘的恶心东西。几十个小时的计算机辅助设计之后，[3DprintedLife]拥有了自己的切皮机器人，它也能切菜。

这台脱壳机 9000 实质上是一台旋转台上的双轴自动切纸机。它使用树莓 Pi 4 和 OpenCV，用一把钝的一元店刀寻找并破坏面包皮。除了紧凑的设计，我们最喜欢的部分是定制控制板中的固件限位开关。步进驱动器有一个奇特的功能，称为 StallGuard，它不断读取反电动势，以确定电机的负载。如果你让它在电机碰到轨道末端并停止之前给你做标记， *bam* ，你就有了一个固件限位开关。休息后，看它去掉面包皮，切很多带脸的胡萝卜。

这与我们最近看到的长相危险的机器人相去甚远。还记得这个剪发装置吗？

 [https://www.youtube.com/embed/FJZa5K6Dk48?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FJZa5K6Dk48?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

