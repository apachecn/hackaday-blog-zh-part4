# 如何在 DJI Mavic Mini 上使用替代电池

> 原文：<https://hackaday.com/2021/01/25/how-to-run-alternative-batteries-on-the-dji-mavic-mini/>

如今，充电电池无处不在，让我们摆脱了使用一次性电池的费用和麻烦。然而，与此同时，许多制造商要求他们的设备只能使用他们自己的官方电池。[【aeropic】并不喜欢这个，所以建造了一个电路让他的 DJI Mavic Mini 用他喜欢的任何电池飞行。](http://aeropic.free.fr/B0B/)

Mavic Mini 使用 I2C 与官方包通信，这使得黑客攻击相对简单。[aeropic]建造了一个昵称为 B0B 的板，它告诉无人机它想听到的内容，并让它在安装了非官方电池的情况下启动。该电路使用 PIC12F1840 与无人机通话，包括报告所安装电池的电压。值得注意的是，它只监测整个包，然后分压以表示单个电池的值，但在典型使用中这应该不是一个大问题。与一些 3D 打印组件结合在一起，它允许您为 Mavic Mini 构建自己的廉价包，只需一个 PCB 和几个 18650 单元。

很高兴看到黑客们走出去，做着面包和黄油的工作来绕过限制性的工厂 DRM 措施，无论是在音乐、打印机墨盒还是无人机电池上。[我们甚至看到了出现在垃圾箱上的祸害。休息后的视频。](https://hackaday.com/2015/01/19/cracking-litter-box-drm/)

 [https://www.youtube.com/embed/pL0dGoH2AC4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pL0dGoH2AC4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

