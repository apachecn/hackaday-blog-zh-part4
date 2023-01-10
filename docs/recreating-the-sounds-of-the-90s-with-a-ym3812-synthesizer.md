# 用 YM3812 合成器再现 90 年代的声音

> 原文：<https://hackaday.com/2022/12/07/recreating-the-sounds-of-the-90s-with-a-ym3812-synthesizer/>

x86 PC 在 20 世纪 90 年代初成为主流游戏平台的一个原因是像 AdLib 和 Sound Blaster 这样的廉价声卡的存在。由于雅马哈的 YM3812 芯片，也称为 OPL2，与个人电脑扬声器微弱的嘟嘟声相比，这些扬声器的音质有了巨大的飞跃。[泰勒]对各种 OPL 系列芯片进行了详细的研究，并撰写了描述其操作的综合指南。

[Tyler]首先解释 FM 合成的理论。基本思想是，你产生不同频率的正弦波，通过混合和调制将它们组合起来，然后随着时间的推移调整它们的强度。通过这种方式，在芯片的九个声道上进行一些简单的操作，就可以产生从清晰的音符到混乱的噪音等多种多样的声音。然后，他深入研究了 YM3812 芯片的细节，包括实现所有这些操作的 279 种不同的寄存器设置。

[Tyler]研究的最终目标是设计一个适合标准模块化合成器的 YM3812 EuroRack 模块。他将在未来的博客文章中详细介绍电路板的设计和构造，但他已经展示了成品，并在下面嵌入的视频中演示了其功能。如果你是 FM 合成的新手，想要重现那些神奇的 DOS 游戏声音，这是一个很好的介绍。

当然，你也可以将 OPL2 芯片连接到你的 DOS 电脑上，无论是通过传统的声卡还是通过并口[。世嘉 Genesis 的相关 YM2612 也使](https://hackaday.com/2018/06/07/vaporwave-for-the-parallel-port/)[成为一个优秀的合成器](https://hackaday.com/2019/05/15/midi-synthesizer-from-a-sega-genesis/)。

 [https://www.youtube.com/embed/k7A3xwO2308?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/k7A3xwO2308?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

