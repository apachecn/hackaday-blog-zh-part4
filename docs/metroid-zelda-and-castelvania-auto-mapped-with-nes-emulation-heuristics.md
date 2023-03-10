# 用 NES 模拟和试探法自动绘制的银河战士、塞尔达和卡斯特尔瓦尼亚

> 原文：<https://hackaday.com/2018/08/30/metroid-zelda-and-castelvania-auto-mapped-with-nes-emulation-heuristics/>

NES 是 20 世纪 80 年代辉煌时代的旗舰游戏机之一。该平台上许多最受欢迎的游戏都包含某种滚动屏幕的冒险——Metroid、Super Mario 和 Zelda 都使用了这种常见的技术。对于许多游戏来说，跟踪地图是一项巨大的工作，意味着在绘图纸上手工绘制地图，或者使用发表在*任天堂 Power* 杂志上的截图。现在有更好的方法。【丹尼尔】着手[自动绘制这些巨大的二维世界](http://prilik.com/blog/wideNES)，开发他称之为 WideNES 的软件来完成这项工作。

WideNES 是[Daniel]自己的 NES 模拟器的附加软件。作为仿真器的一部分，WideNES 可以轻松读取 NES 图像处理单元(PPU)的各种寄存器。PPU 的寄存器用于控制 NES 图形的背景和子画面层的显示，通过监控这些，可以检测和绘制出各种 NES 游戏中关卡的显示。

这是一款有趣的软件，它依赖于对 NES 显示硬件的透彻理解，以及一些处理边缘情况的巧妙技巧的实现，如*《塞尔达传说》*中的垂直滚动或*《恶魔城》——*等游戏中的房间变化。感知哈希的使用尤其天才。[在项目页面](https://prilik.com/ANESE/wideNES)上有资源和更多信息，包括一个 GitHub 链接，如果你有兴趣进入正题的话。

我们对 WideNES 能够如此清晰地描绘出这些昔日游戏的方式印象深刻，并迫不及待地想知道该项目下一步的走向。[Daniel]指出，集成到更流行的模拟器中应该没有太多麻烦。如果这还不够的话，[看看这个反仿真任天堂黑客](https://hackaday.com/2018/05/31/reverse-emulating-nes-nintendception/)。

【感谢迈克尔的提示！]