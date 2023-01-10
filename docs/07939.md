# 用可编程电源向旧车床传授新技巧

> 原文：<https://hackaday.com/2020/10/04/teaching-an-old-lathe-new-tricks-by-handing-z-control-to-a-stepper/>

问问那些花时间站在磨机或车床前的人，他们会告诉你有些操作会变得乏味。当你需要以 0.030 英寸的增量将不锈钢杆调低 1/4 英寸时，你会有很多时间来反思为什么不在来回转动曲柄时购买合适尺寸的股票。这就是丝杠的用武之地——大多数车床都有一个齿轮驱动的丝杠，可以用来驱动 z 轴(与旋转轴平行的轴)。它不是 CNC，但这种类型的传动装置使生活更容易，它已经存在很长时间了。

当托尼·戈阿彻创造了[丝杠伙伴](http://funwithelectrons.blogspot.com/2020/09/leadscrew-buddy-upgrade-for-old-lathe.html)时，他将这个想法向前推进了几步。他将一台漂亮的 1949 年 Myford 车床与一个 Arduino、一个步进电机和一些按钮结合起来，为这台古董机器增加了一些真正有用的功能。通过将丝杠与车床的齿轮箱分离，并通过步进电机驱动它，他实现了更精细的可变进给速度。

如果这还不够的话，[托尼]用一个旋转编码器在一个自制的数字读数器上显示刀具的位置(DRO)。 持续时间是一个“转到”命令。一旦[Tony]设定了原点位置，他就可以命令 z 轴以给定的速度移动到设定点。这不仅使车削更容易，而且使加工过程更容易重复，并使零件表面更光滑。

对于那些习惯使用现代数控车床的人来说，这些功能似乎并不陌生，但对于我们大多数车库机械师来说，[Tony]的实现是一个令人兴奋的发现，让我们可以加快我们的转向游戏。它也很好地符合我们在 Hackaday 这里看到的车床项目的范围——从[超低技术](https://hackaday.com/2020/06/29/build-a-lathe-like-its-1777/)到[可笑精确的](https://hackaday.com/2019/10/31/high-precision-air-bearing-cnc-lathe-and-grinder/)。

 [https://www.youtube.com/embed/_x8gHGMyXSo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_x8gHGMyXSo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

