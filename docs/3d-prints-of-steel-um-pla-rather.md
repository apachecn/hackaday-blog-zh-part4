# 钢铁——嗯——PLA 的 3D 打印

> 原文：<https://hackaday.com/2021/08/12/3d-prints-of-steel-um-pla-rather/>

需要钢梁？你可以 [3D 打印 PLA 梁](https://reprapltd.com/3d-printed-beam-that-is-as-stiff-as-steel/)根据【RepRap】与同等重量的钢梁一样坚固。FreeCAD 的 [Python 代码生成了一个重复结构，特别适合可以打印任意长度光束的带式打印机。当然，请记住，给定两个重量相同的东西，如果一个是钢做的，另一个是 PLA 做的，那么钢的会小一些。](https://github.com/RepRapLtd/Infinite-Z-Beam)

梁是重复的四面体，非常坚固，外表面有许多材料来抵抗弯曲。每个横梁末端都有一个整齐的块，上面有一个接线孔和一圈小孔，允许您以 30 度的旋转增量将横梁安装到物体上或彼此安装。

事实证明，这些洞对于 FreeCAD 几何引擎来说是一个烂摊子，所以脚本实际上做了我们只能称之为黑客的事情。它随机改变切割圆柱体的尺寸。这种变化太小了，以至于在最终的打印结果中看不出来，但却大到足以打破扰乱软件的一致性。

你不一定要有带式打印机来制作这些光束，但如果没有，你只能打印一个和你的打印床一样长的光束。我们想知道我们是否会开始看到使用这些光束作为框架元素的 3D 打印机？这似乎是有道理的。

如果这让你有做带式打印机的冲动，[继续吧](https://hackaday.com/2021/02/25/turn-an-ender-3-into-a-belt-3d-printer-of-your-very-own/)。我们之前已经讨论过 [3D 打印挤压](https://hackaday.com/2021/02/25/turn-an-ender-3-into-a-belt-3d-printer-of-your-very-own/)，但这看起来可能更实用。