# 核心 XY 解释

> 原文：<https://hackaday.com/2019/11/12/core-xy-explained/>

如果你正在建造一台 CNC 机床，一台 3D 打印机，甚至一台绘图仪，你需要在 X 和 Y 两个方向上运动。有许多方法可以实现这一点，例如，一些打印机在 X 方向上移动工具，在 Y 方向上移动床身，而另一些打印机在 Y 方向上移动整个 X 托架，还有更多打印机使用 delta 机构。然而，最古老的方法之一是核心 XY 方法。这很有趣，因为两个电机都保持静止，而业务端完全通过皮带或绳索移动。这类似于 H-Bot 技术，但有一些不同。[Michael Laws]有一个视频(见下文)解释了两个固定电机如何在 XY 区域内移动刀具。

核心 XY 背后的思想至少可以追溯到旧的制图桌。你可以把它想象成由同一根带子的两端握住的一个物体。随着皮带一端变短，另一端变长。皮带的排列使得一个马达的运动导致工具以 45 度角运动。这意味着你必须移动两个电机走直线。

这样做有一些明显的优势，但是——当然——也有一些代价。没有完美的世界，你的每一个选择都会以某种方式改变你的机器的设计。

视频还谈到了其他一些机制，包括 delta 打印机。控制这些打印机需要一些额外的数学运算，尽管核心 XY 机械装置的数学运算并不复杂。

我们已经看了一些在之前使用[核心 XY 的机器。我们还将该机制与类似的](https://hackaday.com/2018/08/03/classy-corexy-build-breaks-down-the-design-pinchpoints/) [H-Bot 设计](https://hackaday.com/2016/02/29/design-analysis-core-xy-vs-h-bot/)进行了比较。

 [https://www.youtube.com/embed/_ramiM3KHYE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_ramiM3KHYE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

