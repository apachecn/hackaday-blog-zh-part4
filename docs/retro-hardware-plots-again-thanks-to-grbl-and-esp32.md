# 得益于 Grbl 和 ESP32，复古硬件再次崭露头角

> 原文：<https://hackaday.com/2019/10/24/retro-hardware-plots-again-thanks-to-grbl-and-esp32/>

当谈到建立一个新的数控机床，你有一个广阔的世界的控制器板可供选择。无论你是在建造一台 3D 打印机还是一台数控等离子切割机，你都有机会找到一台符合你需求和预算的控制器。不过，如果你想在个人电脑革命早期的笔式绘图仪上增加数控系统，就没那么难了。

[Barton Dring]刚刚发布了一个五部分系列的最后一部分，其中他记录了将 Atari 1020 绘图仪置于 CNC 控制之下。该绘图仪是 20 世纪 70 年代后期雅达利 6502 系列机器的外围设备；小型卷轴式圆珠笔绘图仪的内部也出现在 Commodore、Tandy 和 TI 版本中。[Bart]的目标是除了控制器之外，不要在这个机械简单的设备上添加或修改任何东西。这说起来容易做起来难，因为单极步进电机控制着笔的位置和纸卷，而且提笔机构使用的是螺线管。对这些的支持必须添加到[他的 Grbl_ESP32 固件](https://hackaday.com/2018/07/26/grbl-ported-to-the-esp32/)中，正如处理绘图仪中缺少归位开关一样，并使 Grbl 工具改变命令适应笔颜色改变机制，该机制通过将笔杆撞向右侧的托架挡块来旋转笔杆。股票控制器被一个定制的印刷电路板取代，它完全适合外壳，有足够的空间备用。下面的视频展示了它绘制出一个令人困惑的相关样本。

从[定制杯垫](https://hackaday.com/2018/12/26/make-an-impression-at-the-bar-with-a-cnc-coaster-plotter/)到[木制镍币](https://hackaday.com/2018/12/26/make-an-impression-at-the-bar-with-a-cnc-coaster-plotter/)再到[复杂的弦乐艺术](https://hackaday.com/2019/02/23/polar-platform-spins-out-intricate-string-art-portraits/)，【巴特】确实让 Grbl 经受了考验。不过，我们真的很喜欢这种复古重做，并完全支持他声明的将更多旧硬件转换为 Grbl_ESP32 的愿望。

 [https://www.youtube.com/embed/XTdoDOojJFQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XTdoDOojJFQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

