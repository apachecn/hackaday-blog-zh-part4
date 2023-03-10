# 嘿，先生模拟器，给我几乎任何经典平台！

> 原文：<https://hackaday.com/2021/09/12/hey-mister-emulator-gimme-almost-any-classic-platform/>

我又回到了 Hackerspace Gent 的 NewLine 会议上的另一个演讲，这是我周末与那个国家的黑客社区交往时纵情畅饮比利时美食和啤酒的结果。这次[是来自【Michael Smith】的 MiSTer 项目的概述，](https://www.youtube.com/watch?v=OI-UCpfokeU)是一个多仿真器，使用 FPGA 来交换从早期的 PDP 小型机到 80486SX PC 的所有实现。

它的核心是[一个包含英特尔 Cyclone SoC/FPGA](https://www.terasic.com.tw/cgi-bin/page/archive.pl?Language=English&CategoryNo=165&No=1046) 的开发板，必须添加一个 USB 集线器，然后进行内存升级，以运行除最简单内核之外的所有内核。一旦硬件被处理好，就好像没有经典的平台没有核心一样，快速浏览一下[的先生论坛](https://misterfpga.org/)就能证明这一点。我们可以在 SNES 和 NED 平台之间无缝切换，甚至在运行 Commodore 64 演示时切换不同的 SID 芯片版本。

有许多不同的途径可以实现像样的仿真器设置，无论是使用硬件、软件还是两者的结合。虽然不太可能有像这款一样多功能的，但我们猜测随着它的进一步发展，它将成为任何游戏玩家显示器或电视下面的固定设备。这是单平台 FPGA 仿真器的一个进步，这是肯定的！

 [https://www.youtube.com/embed/OI-UCpfokeU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OI-UCpfokeU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

