# 克隆的内存模块修复损坏的示波器

> 原文：<https://hackaday.com/2021/06/17/cloned-memory-module-fixes-broken-scopemeter/>

找到损坏的测试设备并修复它使其重新工作是黑客们由来已久的传统。如果你幸运的话，那辆在易贝买的车会因为一个爆裂的保险丝或几个坏电容而被 DOA，用剪刀和烙铁做一点工作会为你赢得一件不错的测试装备和吹牛的权利。

不过，有些维修是自成一类的，比如为数字示波器移植记忆模块。故事开始于一段时间以前，当时[反馈回路]从易贝捡了一小批坏掉的福禄克 199C 示波器。它们被列为“仅零件”，这从来都不是一个好兆头，而且这些仪表确实处于各种拆卸和不完整的状态。

下面视频的主题缺少几个重要的部分，比如电池和电源连接器，但最关键的是它的内存模块。幸运的是，另一个仪表有一个很好的模块，使得逆向工程成为可能。这项工作始于从 PCB 中释放两个 RAM 芯片和两个 flash 芯片，所有这些芯片都采用 BGA 封装。从那里，每个芯片进入内存编程器读取其图像，然后被写入新的芯片。无芯片电路板被复制——这对于一个六层 PCB 来说是一个不小的任务——并且订购了新的电路板。在焊接上编程芯片和几个无源元件后，模块被插上电源，使得电表如同新的一样。

虽然我们都爱他们，但显然有许多测试装备收集者的阵营。你有你的[福禄克粉丝](https://hackaday.com/2013/08/23/upgrading-a-fluke-multimeter-with-a-masterful-addition/)，你的[惠普粉丝](https://hackaday.com/2018/08/29/faded-beauty-dmm-gets-an-oled-makeover/)，[财大气粗的吉时利人群](https://hackaday.com/2018/08/05/how-much-current-does-that-thing-draw/)——但是[每个人都喜欢泰克](https://hackaday.com/2016/07/25/alan-wolkes-how-to-use-an-oscilloscope/)。

 [https://www.youtube.com/embed/C1NHDiM2-n0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/C1NHDiM2-n0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

