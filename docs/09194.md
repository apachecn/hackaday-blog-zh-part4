# 简单的传感器使灯丝测量变得轻而易举

> 原文：<https://hackaday.com/2021/02/07/simple-sensor-makes-filament-measurements-a-snap/>

现代 FDM 打印机灯丝的制造公差有多严格？好奇的头脑想要知道，当这样的头脑被像[托马斯·桑莱德勒]这样方便的人所依附时，你最终会得到像[这个自制细丝测量装置](https://www.youtube.com/watch?v=-0D30mfIVd0)这样的东西来收集你所寻求的数据。

这个建筑的核心并不像人们可能想象的那样，是一些奇特的激光设备来光学测量灯丝的直径。这些是存在的，但它们是昂贵的工具，最好留给制造商，他们在生产线上使用它们来确保灯丝符合他们的规格。相反，[托马斯]使用了一个非常聪明的自制设备，它依靠霍尔效应传感器和杠杆上的磁铁来完成这项工作。杠杆连接到一个滚柱轴承上，当细丝缠绕通过传感器时，滚柱轴承骑在细丝上；直径的变化被杠杆臂放大，杠杆臂摆动霍尔传感器上的磁铁，产生与灯丝直径成比例的信号。

完整的测试装置有一个电机驱动的进料和卷取卷轴，以及三个传感器，在半径周围的三个不同点测量细丝；将测量值平均在一起，以说明任何小规模的不规则性。[Thomas]将代表不同制造商和材料的几个不同线轴穿过机器；我们不会破坏下面视频中的结果，但可以说，如果你从一个信誉良好的供应商那里购买，你可能没什么可担心的。

当我们看到灯丝传感器时，通常更多的是“那里/不在那里”的变化，以防止打印机在卷轴用完后盲目进行。在之前，我们已经见过一些，但这是对那个概念的一个巧妙的转变。

 [https://www.youtube.com/embed/-0D30mfIVd0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-0D30mfIVd0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Baldpower]的提示。