# 梯度填充将更多的塑料放在你想要的地方

> 原文：<https://hackaday.com/2020/01/20/gradient-infill-puts-more-plastic-where-you-want-it/>

为 3D 打印零件设置填充总是很棘手。高填充部分强度高，但打印时间较长，而低填充打印时间较短，但内部较弱，并且存在填充图案之间表面层下垂的危险。【Stephan】有更好的答案:[渐变填充](https://www.cnckitchen.com/blog/gradient-infill-for-3d-prints)。你可以看下面的视频，在 GitHub 上找到他的 [Python 代码。](https://github.com/CNCKitchen/GradientInfill)

这个想法很简单。在大多数情况下，承受应力的零件在表面附近会有较高的应力。与在应力较低的地方添加塑料相比，在那里添加更多的材料会使零件更坚固。[Stephan]之前已经进行了有限元分析，以确定最佳填充模式，但这有点难以做到。由于大多数零件可以遵循边缘多中心少的规则，所以除了少数特殊情况外，渐变填充是有意义的。

当然，真正的问题是:如何用这种填充材料制造零件？一些切片机有填充设置，几乎可以让你有。然而，它们的设置并不容易。例如，KISSSlicer 的付费版本将采用灰度图像来设置填充密度。[Stephan]注意到，Cura——可能还有大多数其他切片器——在 g 代码中添加了注释，以显示不同功能(如填充)的起始位置。通过在填充过程中更改挤出量，您可以使用相同的基本图案，但仍然可以获得所需的渐变。

他编写了一个简单的程序，在 g 代码发送到打印机之前对其进行后处理。他计算与零件外部的距离，并以此为基础更改挤出量。这是因为他使用了一种不寻常的填充类型，这种填充类型已经存在于小线段中。然而，对于更传统的填充图案，线很长，所以他的程序必须将线切成更短的段，然后应用该算法。当然，这会导致文件变大。

有一些规定。您需要在填充之前打印墙，并且需要设置相对拉伸。如果你的切片器没有发出注释来标记填充的开始和结束，那将是一个问题。即使这样，如果评论和 Cura 的不一样，你可能需要修改代码来适应。或者直接用 Cura 切片。

测试结果很好。零件更坚固，尽管在某些情况下，简单地增加填充物会得到相同的结果。正如[Stephan]所指出的，它可能并不完美，但对许多部分都是有用的。

我们对[后处理 g 代码](https://hackaday.com/2015/07/22/better-3d-prints-by-mixing-slicing-techniques/)并不陌生。无论如何，对于某些工作，你只需要[编写自己的 g 代码](https://hackaday.com/2018/11/14/3d-print-springs-with-hacked-gcode/)。

 [https://www.youtube.com/embed/hq53gsYREHU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hq53gsYREHU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

