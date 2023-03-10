# 这种 3D 打印的“无叶片”风扇成本低廉

> 原文：<https://hackaday.com/2020/09/01/this-3d-printed-bladeless-fan-gets-it-done-cheap/>

在戴森推出他们的“无叶片”风扇后不久，一批更便宜的克隆产品已经开始进入市场。但是这个由[精英蠕虫]创作的 3D 打印版本肯定是最经济实惠的概念之一。如果你有一台 3D 打印机，我们敢打赌你已经有了制造自己的 3D 打印机所需的大部分零件。

[![](img/7965335e104f409b114416eae7d88d20.png)](https://hackaday.com/wp-content/uploads/2020/08/3dpfan_detail.jpg)

See, there’s a blade.

说清楚，当然有刀片。很明显，它们不是魔法。风扇只是很小，而且[藏在底座](https://hackaday.com/2009/10/14/it-has-blades-dysons-little-white-lie/)里面。空气从侧面和底部被吸入安装在装置顶部的环中。当空气最终离开环中的狭缝时，由于柯恩达效应，它会“粘”在边缘，并在中心产生一个低压区。这是一种奇特的说法，你从这些小工具中获得的气流比正常情况下小风扇能够获得的气流大几倍。总之，理论上是这样的。

我们不能保证在这个 3D 打印版本中所有的物理都正常工作，但在休息后的视频中，它显然移动了大量的空气。它也很吵，但这是预料之中的，因为它使用的是无刷电机。为了让它旋转，[Elite Worm]正在使用一个连接到标准 RC 电子速度控制(ESC)的 Digispark ATtiny85。MCU 读取安装在风扇侧面的电位计，并将其转换为电子悬架控制所需的脉宽调制信号。

除了电子产品，基本上这个项目的每一个部分都是用标准的桌面 3D 打印机打印出来的。一个令人印象深刻的成就，尽管出于安全考虑，我们可能会选择商用螺旋桨。另一方面，风扇的底座应该很好地容纳它在每分钟几千转的速度下爆炸时产生的弹片。大概吧。

 [https://www.youtube.com/embed/mB9hSCZ4qo8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mB9hSCZ4qo8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

