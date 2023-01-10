# 2022 年 Hackaday 奖:Baffatari 2600 为复古计算机增加了 atari 兼容性

> 原文：<https://hackaday.com/2022/06/29/hackaday-prize-2022-the-baffatari-2600-adds-atari-compatibility-to-retrocomputers/>

就像今天的英特尔-AMD 双头垄断一样，20 世纪 70 年代和 80 年代的家用电脑 CPU 市场由两家公司主导:Zilog 的 Z80 和 MOS Technology 的 6502 处理器。但与今天不同的是，即使两台电脑有相同的 CPU，也不意味着两台电脑的软件兼容:内存布局、视频接口和存储介质的差异意味着为 Atari 2600 开发的软件不能在 Apple I 上运行，尽管两台电脑共享相同的基本 CPU 架构。

[Augusto Baffa]的最新现代反计算机设计 Baffatari 2600 巧妙地展示了这两台计算机之间的差异只是表面现象。Baffatari 是一个插件板，将 Atari 2600 功能添加到[Augusto]早期的 Baffa-6502 系统中，该系统旨在与 Apple I 兼容。由于苹果和雅达利都是由 6502 CPUs 驱动的，所以只需要交换一些外围设备就可以将一个换成另一个。

Baffatari 板上有两个对 Atari 2600 架构至关重要的芯片:包含 RAM 和操纵杆接口的 6532 RAM I/O 定时器(RIOT ),以及处理图形和音频的电视接口适配器(TIA)。这些芯片连接到 Baffa-6502 的系统总线，使主 CPU 能够与它们通信并运行 Atari 2600 软件。在下面嵌入的视频中，可以看到 Baffa 系统上运行的几款经典游戏。

基本想法类似于[这个 RC2014 插件板](https://hackaday.com/2018/06/22/theres-rc2014-life-in-the-tms9918a-display-chip-yet/)，使基于 Z80 的 retrocomputer 能够运行 MSX 和 Colecovision 游戏。事实上，[Augusto]也为[他早期的 Z80 项目](https://hackaday.com/2022/03/06/retro-serial-terminal-uses-modern-chips-to-get-cp-m-machine-talking/)建造了这样的板。

 [https://www.youtube.com/embed/aCWfbqCGWRI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aCWfbqCGWRI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[hack adayprize 2022](https://prize.supplyframe.com)主办单位:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)