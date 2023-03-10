# 设计移除支撑

> 原文：<https://hackaday.com/2022/12/05/designing-to-remove-supports/>

如果你想用 FDM 打印机 3D 打印任意形状，你经常会发现你需要支架。如果您有可溶解的支持材料，这可能不是一个大问题，但如果您使用与打印时相同的支持材料，则移除它可能会很困难，这取决于支持材料和切片机的位置。至少，它将需要更多的时间和灯丝来打印，至少需要一些后期处理。[Slant 3D]断言你总是可以使用[倒角和圆角](https://www.youtube.com/watch?v=FMs-VGAu_PQ)重新设计零件，以避免一开始就需要支撑。看视频，下面。

当然，有时候你只需要把零件翻转过来。例如，讨论中的部分(这只是一个例子)可以旋转以避免支撑，但这当然不是重点。然而，圆角可能仍然需要支撑，所以你最后不得不做双圆角来真正避免支撑。

根据视频，答案是倒角。角度的稳定变化易于印刷，尽管不是所有的设计都允许陡峭的倒角。所以选择角度是关键，你甚至可以混合倒角和圆角。

创建倒角和圆角可能容易或困难，[取决于你选择的 CAD 软件包](https://hackaday.com/2022/11/28/taking-distance-based-cad-to-the-next-level/)。众所周知，OpenSCAD 很难添加这些东西，但是您可以使用 FreeCAD，它可以与 OpenSCAD 进行互操作，从而使添加变得更容易。也有一些[图书馆](https://www.thingiverse.com/thing:1305888)可用。说到 FreeCAD，我们看到该工具用于另一种方法来避免支持:[打印平面和折叠](https://hackaday.com/2022/05/01/bend-your-prints-to-eliminate-supports/)。

 [https://www.youtube.com/embed/FMs-VGAu_PQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FMs-VGAu_PQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

