# 驱动小型电机的多种方法

> 原文：<https://hackaday.com/2018/11/19/many-ways-to-drive-a-small-motor/>

用于触觉反馈和振动的微型马达有多种形状和尺寸。最常见的是“偏心旋转质量”(ERM)类型，它只是在一个小电机上旋转不平衡的重量，并以两种形式封装。经典的是寻呼机“寻呼机电机”，它看起来就像一个小巧可爱的电机和矮胖的圆柱形“煎饼样式”。erm 使用简单，但与新一代的“线性共振致动器”相比，其响应不精确。与 ERM 中的电机不同，LRA 通常是弹簧上的封闭质量，弹簧靠近线圈，线圈来回推动质量。LRA 这个名字可能不太熟悉，但苹果的品牌实现 Taptic Engine 可能更容易识别。![](img/e93205f3f914a35189a60316fa8e59b9.png)

[Precision Microdrives]是这类器件的供应商，碰巧拥有一套令人愉快的应用笔记，涵盖任何可以想象的相关主题。一个很好的起点是这本关于在电池供电环境中用恒定电压驱动电机的方法的入门书。它从最简单的选项(分压器，duh)开始，通过使用 LDO 或控制器完成其他几个选项。

如果你正在考虑给一个项目添加触觉，并且不知道使用哪种致动器(见:这篇文章的顶部) [AB-028](https://www.precisionmicrodrives.com/content/ab-028-vibration-motor-comparison-guide/) 是一个很好的资源。它深入讨论了不同的选项，以及安装位置、PCB 连接、驱动模式等方面的考虑因素。在他们的网站周围挖掘也产生了一些其他有趣的文件，像[这个关于安装到织物](https://www.precisionmicrodrives.com/content/ab-010-mounting-vibration-motors-to-flexible-materials-clothing/)和其他柔性表面上的文件。或者这个关于[选择 PWM 频率](https://www.precisionmicrodrives.com/content/ab-022-pwm-frequency-for-linear-motion-control/)。