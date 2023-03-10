# 拱廊小行星，现在是彩色的

> 原文：<https://hackaday.com/2018/10/13/arcade-asteroids-now-in-colour/>

小行星是早期街机时代的经典游戏之一。Atari 于 1979 年推出，它依靠 XY 矢量显示器为其基于太空的游戏提供清晰的图形。最初的街机游戏的局限性之一是游戏只能用单一的颜色，白色来渲染。三十多年后，[Arcade Jason]决定看看如何建造一台彩色小行星机器。

![](img/2e0a6c70aab687f1636bec416abaf0b0.png)

The ROM hack also modified the shapes of several in-game objects.

黑客依赖于原始游戏使用四位电阻梯形 DAC 来绘制不同强度级别的向量。通过一些巧妙简单的硬件，这个 DAC 被重新用于表示不同的颜色。它与 74LS08 与门芯片以及一些电阻和二极管结合在一起。三位分别用于红色、绿色和蓝色，第四位用作“白色增强”信号，以区分红色和粉色、深蓝色和浅蓝色等颜色。然后全部连接到一个 RGB 矢量显示器上进行最终显示。在这之后，它只是一个简单的 ROM hack 来设置各种屏幕上对象的颜色。

众所周知，矢量显示器很难很好地拍摄，但很明显，亲自输出是相当令人印象深刻的。制作旧复古游戏的彩色版本实际上是[Arcade Jason]的一个爱好—[我们之前已经展示过他的彩色 Vectrex。](https://hackaday.com/2018/01/03/vectrex-finally-in-color/)休息后的视频。

 [https://www.youtube.com/embed/Dw2TmDtUGm0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Dw2TmDtUGm0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

