# 三叶草计算机:一台现代化的 Z8000 CP/M 机

> 原文：<https://hackaday.com/2022/08/21/clover-computer-a-modern-z8000-cp-m-machine/>

最近在易贝看到一些旧的 Zilog 16 位芯片，[Scott Baker]很好奇，抢购了这些芯片，并为自己建造了一台 Z8000 计算机。一开始是两块板的解决方案，后来他增加了一个显示模块。[Scott]没有像 PC/104 堆栈那样将电路板垂直分层，而是决定将它们平铺起来。他的第一个背板是三角形的，但他选择了正方形，以适应未来的扩展板。组装好的装置类似三叶草，因此被命名为三叶草计算机。

Z8000 是 Zilog 的第一款 16 位微处理器，于 1979 年推出。由于各种原因，它并不是非常受欢迎(维基百科的文章中有一些有趣的细节)。在市场上，英特尔的 8088 和摩托罗拉的 32 位 68000 让 Z8000 黯然失色。有趣的一点是，Z8000 没有使用微码，因此，它的晶体管数量明显少于同时代的产品。Z8000 被用于一些军事应用，尽管它的商业成功有限，但直到 2012 年，它仍然可以从 Zilog 和授权的第二来源获得。

[Scott]的设计将系统分为 CPU 板、内存和串行板以及显示板。一路上，他从 Olivetti M20(为数不多的围绕 Z8000 设计的计算机系统之一)中学到了 20 世纪 80 年代的技巧。他还设法找到了 GitHub 用户[ [4sun5bu](https://github.com/4sun5bu) ]最近对 CP/M 的 Z8000 实现，该实现[Scott]派生并适应了他的项目(参见此处的[项目回购](https://github.com/sbelectronics/z8000))。他成功地让一切正常工作，并移植了一个监视器、Tiny Basic 和 Zork。

查看他的项目评论介绍链接，并在休息时间下方的视频中观看它的实际操作。您曾经使用或遇到过 Z8000 吗？请在评论中告诉我们！

 [https://www.youtube.com/embed/SvSKPFVnW94?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=753&wmode=transparent](https://www.youtube.com/embed/SvSKPFVnW94?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=753&wmode=transparent)

