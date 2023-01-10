# 树莓派皮可用作晶片机

> 原文：<https://hackaday.com/2021/08/05/raspberry-pi-pico-used-as-a-transputer/>

当一个 4 美元的微控制器开发板可以成为 20 世纪 80 年代的尖端技术时，你不能假装这种感觉。这就是【阿门】用树莓派微型电脑制造的工作晶片机[的情况。](http://trochilidae.blogspot.com/2021/07/stack-based-with-os-in-hardware.html)

要全面了解晶片机，你应该[看看【Jenny List】关于主题](https://hackaday.com/2019/04/19/retrotechtacular-transputer/#more-352224)的更长的文章，但归结起来，我们谈论的是一种几乎被遗忘的芯片架构。针对并行计算，每个晶片机芯片有四个串行通信链路，用于连接其他晶片机。【阿门】从一开始就想玩建筑。当时和今天都很昂贵，找到多个晶片机既困难又昂贵。然而，在 Raspberry Pi Pico 上发现的 RP2040 芯片让他想到了模仿晶片机设计的完美方式。

Pico 板上的 RP2040 芯片有两个可编程输入/输出模块(Pio ),每个模块中有四个状态机。这与四个晶片机链接完全匹配(每个都是双向的，所以需要八个状态机)。此外，链路速度为 10 MHz，这完全在 Pico 的能力范围内，由于 RP2040 的运行速度为 133 MHz，可以想象，仿真内核可以接近原始晶片机的 20 MHz 最高速度。

硬件的提出是成功的。为了了解实际情况，[阿门]采购了一些链接适配器芯片(IMSC011)，通过 Arduino Mega 将它们连接到计算机，以使用键盘和显示器。晶片机架构允许通过 ROM 或通过链接加载代码。后者就是现在运行的。未来的计划是找出一个更好的系统来编译代码，因为目前唯一的方法是在 VM 中的 DOS 上运行原始的 INMOS 编译器。

请听[阿门]在(到目前为止)六个视频系列的第一个中解释该项目。你可以在他的 YouTube 频道上找到其余视频[的链接。](https://www.youtube.com/channel/UCNweFQHar6-JMdXFk-MrOtQ/videos)

 [https://www.youtube.com/embed/MV_q7ltG8gY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MV_q7ltG8gY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

