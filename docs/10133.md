# JavaScript 应用程序使用高级数学让印刷电路板更容易蚀刻

> 原文：<https://hackaday.com/2021/05/19/javascript-app-uses-advanced-math-to-make-pcbs-easier-to-etch/>

我们都记得我们上过的各种数学课中的一系列问题，当无法理解一个困难的概念时，沮丧会溢出到经典问题中，“在现实生活中，我什么时候需要知道这个？”但众所周知，即使是最深奥的数学概念在现实世界中也有应用，如果不能掌握它们，你可能会自食其果。

以 Voronoi 图为例。虽然我们不记得在任何数学课上接触过这些，但事实证明它们在一个看似不相关的领域非常有用:[将 PCB 设计转换为易于蚀刻的方格图案](https://github.com/caiannello/jsVoronoiPCB)。 [Voronoi 图](https://en.wikipedia.org/wiki/Voronoi_diagram)实际上是一个分成不同区域或“单元”的平面，每个区域或“单元”以一个“种子”对象为中心。每个单元格都是一组点，它们与特定种子的距离比与任何其他种子的距离都要近。对于多氯联苯，种子可以用轨迹来表示；将平面分割成这些轨迹周围的单元，会产生易于蚀刻的棋盘格图案。

为了让这一点对 PCB 创作者有用，[Craig Iannello]想出了一个 JavaScript 应用程序，它可以拍摄 PCB 的图像，细化轨迹，并输出适合激光雕刻机的 g 代码。一层喷漆覆盖的空白 PCB，棋盘格图案被刻入油漆中，电路板以通常的方式被蚀刻和钻孔。[Craig]的程序允许在电路板上添加特定功能，如需要特定布线的异形焊盘或迹线。

这不是我们第一次看到 [Voronoi 图被用于 PCB 设计](https://hackaday.com/2020/07/31/transform-kicad-design-to-patchwork-for-isolation-routing/)，但这种方法看起来如此简单，我们很想试一试。它甚至看起来好像也适用于数控板材铣削。