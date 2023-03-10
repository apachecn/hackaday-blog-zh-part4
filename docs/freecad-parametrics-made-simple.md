# freecad 参数化简化

> 原文：<https://hackaday.com/2020/10/09/freecad-parametrics-made-simple/>

简单的绘图程序只是让你像用铅笔一样画画。但是现代程序使用参数模型提供了几个好处。一个是您可以使用参数来更改设计的某些部分，而其他部分会根据您的更改而改变。另一个好处是你可以用一个模型做许多相似但不同的设计。[Brodie Fairhall]有一个关于如何在 FreeCAD 中使用[参数的很好的视频。](http://www.youtube.com/watch?v=fXoRAYv1wHQ)

参数的好处是它们不一定只是常量。你也可以输入公式。例如，您可以将一条线定义为另一条线的两倍。您提供各种约束和参数，FreeCAD 会为您计算出形状，并满足所有的约束和公式。

[Brodie]展示了如何使用电子表格来管理大型项目中的复杂参数，这非常方便。有一个即将推出的功能，将允许您将参数分组到集合中。例如，您可以看到一个 NEMA 步进电机模型，它可以通过从配置表中选择不同的参数，从 NEMA 17 变到另一个尺寸。

当然，OpenSCAD 除了以非常直接的方式进行参数化建模之外，什么也不做。您显式地编码您想要的约束。我们最近也在享受 [Solvespace](https://hackaday.com/2020/07/16/freecad-vs-solvespace/) 。

 [https://www.youtube.com/embed/fXoRAYv1wHQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fXoRAYv1wHQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

