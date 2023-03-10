# 一个小巧的金属探测器

> 原文：<https://hackaday.com/2019/02/26/an-attiny-metal-detector/>

金属探测器曾经是一种完全模拟的仪器，是一种振荡器，当一块金属靠近时，它的频率随着感应线圈的电感而变化。[ukasz Podkalicki]向我们展示了一台更复杂的机器,但明智地使用 ATtiny 13，它并不复杂。

脉冲感应金属探测器在其搜索线圈中感应出一个电流尖峰，并记录由此产生的振荡的衰减。线圈是带有电容的谐振电路的一部分，其磁场中的任何金属都会改变其谐振频率。在[ukasz]的设计中，ATtiny13 使用 MOSFET 向其线圈发射一个脉冲，线圈上的电压通过适当的箝位电路由模拟引脚检测。他的软件会计时，并在探测到金属时发出蜂鸣声。这是一个非常简单的实现，虽然他在视频中向我们展示了它相对较小的线圈更适合检测干墙后面的硬币或电线，而不是定位丢失的宝藏，但可能还有足够的空间进行进一步的实验。

这并不是来自[ukasz]的第一个项目进入这些页面，[他与 ATtiny13 的历史可以追溯到几年前](https://hackaday.com/2016/11/24/tiny-tunes-on-an-attiny13/)。

 [https://www.youtube.com/embed/mc7C9EcBRFI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mc7C9EcBRFI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

