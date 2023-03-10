# AntRunner 是您需要随身携带的卫星天线支架

> 原文：<https://hackaday.com/2022/09/17/antrunner-is-the-satellite-antenna-mount-you-need-to-take-with-you/>

显而易见，如果你想和卫星通信，无论你用什么天线都应该指向那个卫星。我们中的一些人已经手动完成了这项工作，跟随空间站在夜空中的亮点。然而，对于任何比试图捕捉短暂的 SSTV 图像更严重的事情，都需要一个更强大的解决方案。换句话说，一个电动天线旋转器，而来自[Wuxx]的[天线旋转器就是这张票](https://github.com/wuxx/AntRunner)。更好的是，对于那些/p 操作会话，它是便携式的。

旋转器本身是 az-el 设计，带有几个齿轮传动的步进电机。完整的机制设计已经发表了，但是复制应该不会太难。有趣的部分是控制器和软件，它可以与 Gpredict、Hamlib 和 SDR 一起工作，实现自动卫星跟踪。控制器就像运行 GRBL 的 ESP 端口的 ESP32 一样简单。

这是一款便携式天线旋转器，易于使用且受到广泛支持，有什么不喜欢的呢？正如你所料，[这不是我们第一次看到](https://hackaday.com/2016/08/31/antenna-rotation-arduino-style/)。事实上， [2014 年黑客日奖由 SatNOGs](https://hackaday.com/2014/11/13/satnogs-wins-the-2014-hackaday-prize/) 获得，其中包括一个 3D 打印天线定位器。

谢谢[Abe Tusk]的提示！