# 超廉价微控制器驱动可寻址 7 段显示器

> 原文：<https://hackaday.com/2020/05/16/ultra-cheap-microcontroller-powers-addressable-7-segment-display/>

自从一年前向我们的社区公开以来，低于 10 美分价格范围内的各种超便宜的微控制器吸引了很多兴趣，但没有太多的项目。当选择 Atmel 或其他处理器是一个更容易的选择时，他们稍微令人讨厌的编程和 PIC12 衍生的架构带来了一个障碍，但这一障碍并没有因为他们的价格而减轻。但这并不是说它们不会慢慢出现，一个很好的例子来自[Tim]，[他用一个红木微控制器制作了一个可寻址的 7 段显示器](https://cpldcpu.wordpress.com/2020/04/05/addressable-7-segment-display/)。如果你习惯于可寻址的多色发光二极管，这将把这个想法扩展到数字信息的世界。

结果是 PCB 比它所服务的 7 段显示器略大，具有互锁的 0.1”引脚连接器，允许模块的菊花链。这些器件的极低成本使其成为极具吸引力的解决方案。在软件方面，它的驱动方式与可寻址 led 类似，他详细介绍了其协议。固件可以在 GitHub 库中找到[。他将读者引向](https://github.com/cpldcpu/SimPad/tree/master/Toolchain/examples/chainable_display) [Easy PDK 编程器](https://free-pdk.github.io/)和[小型设备 C 编译器](http://sdcc.sourceforge.net/)，这些处理器应该会让任何人感兴趣。