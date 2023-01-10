# 简单的二进制编码十进制手表

> 原文：<https://hackaday.com/2022/05/10/a-simple-binary-coded-decimal-watch/>

模拟和液晶手表都是有用的设计，但最终是主流钟表。使用二进制手表是一种简单的方法，可以让一个人作为技术爱好者脱颖而出，同时给你的黑客朋友留下深刻印象。

我们从[vishalsonindia]获得了一个这样的产品，它使用了一个裸露的 PCB，旨在直接与传统的表带相匹配。板上的单个触觉按钮用于激活手表，在手表的 led 上以二进制编码的十进制显示小时和分钟的当前时间。长按该按钮可将手表置于设置模式，根据需要校正时间。

该手表依赖于 ATtiny85 微控制器，这是一种轻巧紧凑的设计，足以运行一个简单的手表。它与 74HC595 移位寄存器配合使用，以最少的引脚数运行所有的 led，板上还有一个 TP4056 充电电路，以保持锂聚合物电池充满。

像这样的项目是学习各种基本电子技能的好方法，从 PCB 设计到 SMD 焊接，甚至使用移位寄存器等基本逻辑部件。作为奖励，你还可以得到一块很酷的手表。

这些年来，我们已经看到了一些类似的设计，[就像构建它们的黑客一样五花八门](https://hackaday.com/2021/08/06/cool-binary-clock-uses-old-school-leds-and-a-fancy-graphic-pcb/)。休息后的视频。

 [https://www.youtube.com/embed/fd1oudY0hw8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fd1oudY0hw8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

