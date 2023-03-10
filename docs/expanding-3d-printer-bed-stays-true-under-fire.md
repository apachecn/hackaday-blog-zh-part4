# 不断扩张的 3D 打印机床在战火中依然如故

> 原文：<https://hackaday.com/2018/11/16/expanding-3d-printer-bed-stays-true-under-fire/>

很难拒绝[马克·雷霍斯特]带给我们的又一堂好的机器设计课。这一次，【马克】[与*床身因*](https://drmrehorst.blogspot.com/2017/07/ultra-megamax-dominator-3d-printer-bed.html) 热膨胀而变形的无情力量作斗争。

你认为你的打印机变热后尺寸不变吗？好吧，再想想！根据[马克]的计算，当加热时，床可以在 x/y 方向膨胀多达半毫米。虽然 x/y 变形似乎是我们可以忽略的东西，但这并不总是正确的。如果我们的床被牢牢固定在某个位置，那么尺寸的变化只会导致床的扭曲，因为它试图为自己腾出空间。

但是不要放弃。尽管这个问题看起来很危险，但[Mark]介绍了一个经典但实现良好的解决方案:以及可调节的运动学耦合。运动学耦合将床保持在最少的点数，以保持其刚性，同时暴露指旋螺钉以在水平床上拨号。这项技术的特别之处在于，耦合保持床的刚性，同时允许它热膨胀！

这就是“精确约束”设计的妙处。零件仅通过保证特定关系所需的最少数量的点结合在一起。这里，喷嘴 x/y 平面和床之间的关系是*共面性*。即使当床展开时，这种关系仍然存在。这就是魔法。

随着市场上 3D 打印零件的大量涌现，制造打印机变得前所未有的简单！然而，我们很容易把自己困在一个角落里，重新调整一个跳过基本原则基础的糟糕设计。如果你对 3D 打印机设计背后的更多这些原则感到好奇，请查看[Mark]对 [CoreXY 设计](https://hackaday.com/tag/mark-rehorst/)的全面演练。