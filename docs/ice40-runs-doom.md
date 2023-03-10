# Ice40 运行毁灭战士

> 原文：<https://hackaday.com/2021/02/07/ice40-runs-doom/>

规格表是确定给定器件或系统性能的重要工具，但对于工程来说，它并不是一切。然而，规格本身并不能证明一个给定的系统是否能完成一个给定的任务。有时候，你需要实际工作来证明这一点—[正如[Sylvain]所做的，在 iCE40 FPGA 上运行 DOOM。](https://www.youtube.com/watch?v=3ZBAZ5QoCAk&feature=youtu.be)

DOOM 的最低规格要求 386 最低 4MB 内存，但人们普遍认为，运行在 66MHz 的 486 DX2 需要 8MB 内存才能流畅地玩游戏。对于运行 25 MHz RISC V 软核的 Breaker v1.0b 来说，这似乎是一项艰巨的任务，但 RISC V 核的好处是许多指令在单个时钟周期内运行，而这在 486 上需要很多。虽然破冰船上没有太多的 RAM，但在现有的闪存存储上搭载 8MB SPI 设备是一项简单的工作。游戏的控制是通过串行发送到破冰船的按键，而视频是通过带有 HDMI 连接器的 PMOD 视频接口处理的。

[Sylvain]做了很好的工作，解释了工作所需的所有细节，并在 Github 上为那些热衷于复制这一壮举或扩展代码的人提供了文件。音乐明显不存在，但 MIDI 输出可能没有太多麻烦。“它运行厄运吗？”依然是很多平台问的问题，[甚至任天堂新游戏&手表](https://hackaday.com/2020/11/22/doom-running-on-the-nintendo-game-watch/)。休息后的视频。

 [https://www.youtube.com/embed/3ZBAZ5QoCAk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3ZBAZ5QoCAk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

