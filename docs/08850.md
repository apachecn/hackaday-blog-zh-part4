# 黑板变得整洁笔式绘图仪

> 原文：<https://hackaday.com/2021/01/03/blackboard-becomes-tidy-pen-plotter/>

打印机都很好，但它们通常局限于较小的纸张尺寸，并且使用昂贵的墨水。如果你想大规模地制作艺术品，绘图仪是个不错的选择。用一块旧黑板做了一个整洁的例子。

如今，由于广泛的 DIY CNC 和 3D 打印社区，这样的构建非常容易实现。绘图仪由一对步进电机组成，由现成的 RAMPS 1.4 控制器和 Arduino Mega 2560 驱动。电机安装在黑板的顶角，通过一对带齿的皮带移动笔杆，平衡重量以保持稳定。笔杆本身安装了一个简单的永久性标记，并使用伺服系统将笔杆推离纸张进行收回，而不是移动笔本身。系统的控制是通过 [Makelangelo 固件，](https://github.com/MarginallyClever/Makelangelo-firmware)这是一种开源的努力，能够驱动各种各样的 CNC 运动系统。

最终结果是一个简单的绘图仪，使用现成的零件，可以在一张 A1 纸上可靠地绘制大型图形。它产生的干净、连续的线条给我们留下了特别深刻的印象，证明了良好的机械设计。

我们在这些地方看到很多阴谋者；[甚至可以画曲线的旋转型](https://hackaday.com/2020/11/11/rotary-plotter-draws-on-bottles/)。休息后的视频。

 [https://www.youtube.com/embed/YTYxPt15hTQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YTYxPt15hTQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/w_8iHQgj6ss?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w_8iHQgj6ss?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

