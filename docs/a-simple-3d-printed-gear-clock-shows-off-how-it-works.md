# 一个简单的 3D 打印齿轮钟展示了它的工作原理

> 原文：<https://hackaday.com/2021/12/23/a-simple-3d-printed-gear-clock-shows-off-how-it-works/>

模拟时钟内部是美丽的东西，使用华丽的齿轮系在机械美的舞蹈中记录时间。然而，太多时候，复杂性隐藏在里面。然而，这个来自[Tada3]的齿轮时钟设计自豪地展示了它的工作原理。

一个小型步进电机用于运行时钟的运动，这是 28BYJ-48 系列的一小部分。电机每秒钟驱动一次，使齿轮传动系统以一种相当引人注目的方式前进，不知何故在视觉上更有趣。当然，通过对设计的一些修改，也可以很容易地实现连续运动。

步进电机由 Arduino Nano 驱动，它也负责计时。缺少的一件事是实时时钟，如果你希望它保持准确的时间，它应该被添加到设计中。事实上，[包含的 Arduino 草图](https://cdn.thingiverse.com/assets/b9/b2/98/e1/da/ArduinoGearClock.ino.txt)只是使用 delay()函数来计时电机的步进。它让时钟滴答作响，但会很快失去同步。

这个设计还在 YouTube 上由[Mirko Pavleski] 制作的一个视频中重现，显示出这些文件的质量适合在家里自己制作。我们以前也见过一些齿轮时钟设计，从[的激光切割](https://hackaday.com/2021/02/08/this-classy-but-chaotic-gear-clock-keeps-you-guessing/)到[的整齐嵌套](https://hackaday.com/2021/12/12/a-nested-gear-clock/)。休息后的视频。

 [https://www.youtube.com/embed/kMnFwARJKyM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kMnFwARJKyM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

