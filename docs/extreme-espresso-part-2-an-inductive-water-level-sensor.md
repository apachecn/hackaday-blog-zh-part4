# 极端浓缩咖啡，第 2 部分:感应水位传感器

> 原文：<https://hackaday.com/2022/03/08/extreme-espresso-part-2-an-inductive-water-level-sensor/>

[马克·史密斯]一定真的很喜欢他的咖啡，至少从他花了多少力气来摆弄他的浓缩咖啡机来看。

这种感应式水箱传感器是[马克]为他的高端 Rancilio Silvia 机器增加的一系列创新中的一部分——我们假设有人会对这种特性提出质疑，但在我们的书中,[800 美元](https://www.amazon.com/Rancilio-Espresso-Machine-Stainless-13-4-Inch/dp/B00H1OUSD2)对于一台咖啡机来说是一笔不小的开支。我们最近对[做了一系列的改装](https://hackaday.com/2021/09/09/ai-powered-coffee-maker-knows-a-bit-too-much-about-you/)，作为“Espresso Connect”项目的一部分，其中包括一个很酷的数码管条形图来显示机器中的水位。该显示器由该传感器驱动，现在[Mark]已经分享了其详细信息。传感器跨在 1.7 升水箱的壁上，因此不需要穿透。坦克内部是一个轨道，引导铜和 PETG 浮子，密封与食品安全的环氧树脂。

水箱外部紧邻浮轨的是一个长 PCB，上面有几条长而弯曲的走线。这些连接到一个 [LX3302A](https://www.microchip.com/en-us/product/LX3302A) 感应传感器 IC，该 IC 读取浮子内铜块的位置。这大大简化了过程；[Mark]详细介绍了传感器板的设计和校准，并将其连接到位于“Espresso Connect”核心的 Raspberry Pi Zero 中。总之，正如下面的视频所示，这些模块可以精确测量浓缩咖啡的剂量。

我们会说这对于一杯完美的咖啡来说可能有点远，但我们确实尊重这种努力。我们认为这种感应传感器方法有很多不含咖啡因的应用，可能值得探索。

 [https://www.youtube.com/embed/aXZKdm05NeA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aXZKdm05NeA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

