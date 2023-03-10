# 3D 打印机的螺栓堵塞检测

> 原文：<https://hackaday.com/2020/05/19/bolt-on-clog-detection-for-your-3d-printer/>

桌面 3D 打印技术在过去几年里有了长足的进步，但它们仍然很挑剔。这部分是因为消费级机器通常不提供太多的仪器。如果灯丝耗尽或热端堵塞并停止挤压，绝大多数打印机将继续嗡嗡作响，而没有任何显示。

为了防止半成品打印的心痛， [[Elite Worm]一直在研究一种非常聪明的细丝探测器](https://hackaday.io/project/171580-3d-printer-clog-detector)，它可以毫不费力地改装到你的 3D 打印机上。该设计，至少在目前的形式下，除了锁定部分冷却风扇作为一种方便的 DC 电源外，实际上并没有与打印机接口。细丝在通往挤压机的途中简单地通过它，如果它停止移动，而风扇仍在运转(表明机器*应该*正在印刷)，它将发出警报。

这个便携设备内部是一个 Digispark ATtiny85 微控制器、一个 128 x 32 I2C 有机发光二极管显示器、一个蜂鸣器、一个 LED 和一个光敏电阻。一个巧妙的 3D 打印机制在灯丝通过挤压机的过程中抓住灯丝，并利用这种移动来交替阻断和疏通 LED 和光敏电阻之间的路径。如果几分钟后微控制器看不到报警脉冲，它就知道出了问题。

在休息后的视频中，[Elite Worm]将设备安装到他的 Prusa i3 MK2 上，但如果你能找到一个方便的地方安装它，它应该可以在几乎任何 3D 打印机上工作。在视频中密切关注我们最喜欢的部分，使用乳胶气球的颈部为细丝传感器的轮子增加一点牵引力。太棒了。

顺便提一下， [Prusa 试图在 i3 MK3](https://hackaday.com/2018/10/22/a-close-look-at-the-prusa-i3-mk3/) 上解决堵塞检测问题，但最终删除了后续 MK3 上的功能，因为该系统被证明对一些灯丝不可靠。官方的说法是，高质量的细丝很少堵塞，打印机不需要它，但当事情发生冲突时，即使是市场上最便宜的纸张打印机仍然会发出哔哔声，这似乎是一个奇怪的疏忽。

 [https://www.youtube.com/embed/fHWlwqQw9eQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fHWlwqQw9eQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

