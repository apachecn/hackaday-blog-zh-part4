# 3D 打印机灯丝的主动应变消除

> 原文：<https://hackaday.com/2019/02/19/active-strain-relief-for-3d-printer-filament/>

购买 3D 打印机灯丝有点像吃薯片:你不能只吃一根就停下来。你从基本的黑色 PLA 开始，然后你需要一个特殊项目的特定颜色，然后你开始尝试不同的塑料，在你知道之前，你已经有几十个卷轴排队。问题是，除非你把正在使用的卷轴移到打印机上方，否则当打印机吸住灯丝时，灯丝可能会变得有点难以控制。怎么办？

为你的细丝收集建造一个主动应变消除系统怎么样？这就是[丹尼尔·哈拉里]选择做的事情，我们不得不说，这看起来非常巧妙。这样做的目的是，无论卷轴相对于打印机的位置如何，在细丝进入打印机的挤压机之前，保持细丝松弛。主动钻头有点像低力挤压机，使用一对老式 2D 打印机的压轮在需要时放出细丝。一个由 3D 打印漏斗和铜线接触环组成的智能传感器，可以检测到打印机何时收紧了细丝的所有松弛部分，并触发馈电线的释放。在一个不错的接触，饲料电机是由一对夫妇的 555，而不是一个微控制器控制。下面的短片展示了进给器被触发并放出更多的松驰。

归根结底，这只是一系列灯丝管理项目中的又一个，从[干燥箱](https://hackaday.com/2018/02/10/heated-drybox-banishes-filament-moisture-for-under-20/)到[灯丝计量表](https://hackaday.com/2016/12/08/this-old-mouse-keeps-track-of-filament-usage/)到[线轴末端报警器](https://hackaday.com/2017/06/07/improving-mister-screamer-an-80-decibel-filament-alarm/)。这可能有点矫枉过正，但[丹尼尔]花了很多心思，我们一直很感激。

[https://videopress.com/embed/SIhbFBvC?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0](https://videopress.com/embed/SIhbFBvC?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0)