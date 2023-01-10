# 船锚双胞胎得到一点数字帮助停留在频率上

> 原文：<https://hackaday.com/2022/03/11/boat-anchor-twins-get-a-little-digital-help-staying-on-frequency/>

在业余无线电行业，像老德雷克装置[斯科特·m·贝克博士]在他的无线电室里拥有的设备通常被称为“船锚”。它指的是又大又重的收音机，与设计时的艺术水平相比，可能有点过度设计了，实际上，这个名字带有贬义是一种耻辱，因为有些设备在制造后的半个世纪或更长时间里仍然坚如磐石。

但旧设备通常更难使用，至少与内置微控制器和更稳定振荡器的新型收音机相比是如此。为了让他的 20 世纪 70 年代的德雷克“双胞胎”接收器和发射器的设置更有趣，斯科特想出了这个基于树莓 Pi 的简洁的 DDS-VFO 项目来保持他的船锚漂浮。与 Drake 接收机中的原始机械调谐可变频率振荡器相比，直接数字合成方法保证了更高的稳定性，意味着更少的旋钮微调以保持频率。

DDS-VFO 所用的硬件实际上非常简单，只是一个 Raspberry Pi Zero W 驱动一个基于 AD9850 的信号发生器模块。向双胞胎发送信号是另一回事。这是通过接入连接两个单元的注入电缆来实现的，这意味着处理信号衰减需要一些复杂的电路。[Scott]还增加了一些便利设施，如数字频率显示器、带曲柄式旋钮的光学编码器来改变频率，以及一系列 Cherry MX 按键开关，用于快速访问不同的功能。

从下面的视频来看，这对双胞胎现在非常坚固，并且更容易使用。这个项目大致是基于最近的一个 panadapter 项目【Scott】为 Twins 的接收器端承担的。

 [https://www.youtube.com/embed/cm6mJycXllU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cm6mJycXllU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

