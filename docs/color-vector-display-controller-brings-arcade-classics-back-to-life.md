# 彩色矢量显示控制器让街机经典重现生机

> 原文：<https://hackaday.com/2022/05/26/color-vector-display-controller-brings-arcade-classics-back-to-life/>

如果您阅读 Hackaday 的时间足够长，您可能会遇到一些黑客，他们在模拟示波器屏幕上制作简单的动画甚至视频游戏。这些黑客通常使用矢量图形，阴极射线管的电子束直接在屏幕上绘制几何形状。这使图像具有独特的外观，与电视和大多数计算机显示器上使用的基于像素的光栅显示器截然不同。

矢量显示器也在 20 世纪 80 年代初的几款街机中使用，包括经典的*暴风雨*、*引力*和*星球大战*。为了比光栅显示器更真实地模拟这些游戏，【Robin Champion】[设计了 vstcm:一个彩色矢量显示器控制器](https://github.com/english1234/vstcm)来轻松驱动 RGB 矢量显示器。

[![Star Wars (1983) displayed on CRT monitor](img/ef016dabc8ceead588545fc62819d1c7.png)](https://hackaday.com/wp-content/uploads/2022/05/VSTCM-playing-Star-Wars.jpg) 该设计基于【Trammell Hudson】和【Adelle Lin】的 [v.st 系统](https://hackaday.com/2015/12/29/32c3-vector-video-games/)，因此具有一个 Teensy 微控制器和几个数模转换器。虽然 v.st 只能连接到示波器等单色 X/Y 系统，但 vstcm 可以与 RGB 监视器配合使用，以近乎完美地模拟基于彩色矢量的游戏。一个定制的软件接口将 vstcm 连接到 AdvanceMAME，这是一个众所周知的 arcade emulator 的特殊版本，有助于连接不同寻常的显示系统。

虽然[Robin]注意到性能没有达到应有的水平，并请求那些熟悉 Teensy 平台的人帮助优化代码，但最终结果看起来确实如此。如果你想构建 vstcm，但找不到矢量监视器，你可以随时[修改传统 CRT](https://hackaday.com/2014/09/18/building-a-vector-monitor-controller/) 的轭。想了解更多关于矢量显示的信息吗？请看[这篇详尽的介绍](https://hackaday.com/2012/12/05/vector-thingy/)。