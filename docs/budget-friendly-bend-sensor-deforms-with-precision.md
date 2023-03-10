# 经济实惠的弯曲传感器精确变形

> 原文：<https://hackaday.com/2020/09/14/budget-friendly-bend-sensor-deforms-with-precision/>

在这一点上，我们非常熟悉基于预算电阻的弯曲传感器，但这种传感器完全不同。[Useok Jeong]和[Kyu-Jin Cho]没有依靠电阻元件，而是设计了一种依靠传感器本身几何特性的[弯曲传感器](https://youtu.be/pna2ue7zv3I)。结果是一个高保真度的测量设备，它是由一个相当广泛的库存零件集合制成的。

我们承认，将这种设备称为*弯曲*传感器可能有点夸张，所以让我们深入了解一些操作原理。我们实际测量的是*累积角*，即沿传感元件长度的所有曲率变形的总和。该传感器由 3 个主要部分组成:一个外部拉伸弹簧基电线护套；一端固定的柔性、张紧的内部线芯；和一个测量金属丝自由端长度变化的小位移传感器。使这种设置工作的秘密成分是外部电线护套或*弹簧导向器*的特殊属性。这里，弹簧导向件实际上*在弯曲时抵抗*被压缩。因为弯曲的内半径保持恒定长度，所以中心线芯被迫伸长。随着多余的电线缠绕在传感器基座上，我们简单地测量我们收集了多少，应用一些数学，并得到一个结果角度！更重要的是，这个把戏背后的人还证明了长度和角度的关系是线性的，R 平方为 0.9969。

这款传感器最棒的一点是，它似乎可以从一个普通的库存零件集合中重现。弹簧导向器(又名:*拉伸弹簧*)可从[麦克马斯特-卡尔](https://www.mcmaster.com/continuous-length-extension-springs/system-of-measurement~inch/od~1-8/)和[坦普莱曼博士](http://stocksprings.drtempleman.com/item/spring-guides/spring-guide/sg-088-020-120)处获得，并且该柔性芯可以容易地用一些钢丝绳代替。

弯曲传感器的新拓扑并不是每天都会出现，更不用说线性传感器了。为了了解更多，这个项目背后的人们已经友好地将他们的研究论文[开放给大家下午阅读。(带上草稿纸！)最后，如果你正在寻找其他与弯曲相关的传感器，看看这个](https://www.mdpi.com/1424-8220/16/7/961/htm)[多弯曲测量设置](https://hackaday.com/2020/06/26/slipping-sheets-map-multiple-bends-in-this-ingenious-flex-sensor/)。

 [https://www.youtube.com/embed/pna2ue7zv3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pna2ue7zv3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

