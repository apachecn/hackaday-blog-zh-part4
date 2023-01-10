# 一个(几乎)单芯片苹果 IIe

> 原文：<https://hackaday.com/2022/12/23/an-almost-single-chip-apple-iie/>

Apple II 是最具标志性的微型计算机之一，詹姆斯·刘易斯决定使用 Apple IIgs 的 Mega-II“芯片上的 Apple IIe”来构建一个微型 Apple IIe。

虽然有一个使用相关 Gemini 芯片的 Apple II 兼容卡，但由于缺乏 Apple II SOC 的文档，最初还不清楚 Mega-II 是否可以在 Apple IIgs 之外工作。经过大量的调试和设计工作后，Mega-II 终于启动了。该系统由三块板组成:Mega-II 和 RAM 板、带 [65C02](https://en.wikipedia.org/wiki/WDC_65C02) 的 CPU 板和视频输出板。

为了简化布线，电路板都是四层 PCB。不幸的是，制造这个系统所需的芯片，尤其是 Mega-II，无法自行获得，必须从现有的 IIgs 中获取。[Lewis]小心翼翼地确保任何拆焊或其他部件的移除都以可逆转的方式进行。如果你想了解所有的细节，可以看看他为项目设计的 [GitHub。](https://github.com/baldengineer/Mega-IIe)

如果你想要另一台基于 6502 的小型计算机，为什么不试试这台基于 Perf+板的[？](https://hackaday.com/2017/02/20/a-6502-retrocomputer-in-a-very-tidy-package/)

 [https://www.youtube.com/embed/vKhUGuODqOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vKhUGuODqOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

