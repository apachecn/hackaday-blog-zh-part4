# 采用非平面切片的 3D 打印 90°悬垂

> 原文：<https://hackaday.com/2021/03/08/3d-printing-90-deg-overhangs-with-non-planar-slicing/>

当对模型进行切片以进行 3D 打印时，零件被分成一堆平坦的 2D 层。但是有一种非平面切片形式的替代方案，其中层可以遵循 3D 曲线。[Rene K. Mueller]更进一步，成功地使用[非平面切片在普通笛卡尔 FDM 打印机](https://xyzdims.com/2021/03/03/3d-printing-90-overhangs-without-support-structure-with-non-planar-slicing-on-3-axis-printer/)上打印了 90 个突出部分。

非平面层已经出现了一段时间，但通常仅限于创建没有层线的平滑曲线。使用悬垂技术的想法已经在[Rene]的脑海中浮动了一段时间，在看到 Hackaday 上的[旋转倾斜喷嘴打印机](https://hackaday.com/2021/01/16/3d-printing-without-support-material-thanks-to-an-additional-axis/)后，他被激励采取行动。这个想法只是让每一层的外边缘向外突出，让每一层都向外突出。[Rene]为此编写了一个圆锥切片算法，将模型分成圆顶状的层，就像洋葱一样。

他做了很多测试，并详细记录了结果。锥形切片与倾斜切片进行了比较，倾斜切片也用于带式 3D 打印机。两者都有一些几何限制。倾斜切片只能在一个方向上打印突出部分，但圆锥切片可以在所有方向上打印，使其在没有任何支撑的情况下创建类似蘑菇的形状。限制是它只能从中心点向内或向外打印。必须分割更复杂的几何图形，并且单独切片每个子体积。切片角度还受到打印头形状的限制，以避免打印头撞上印刷品。

我们认为这项技术有广泛应用的潜力，特别是因为它与大多数现有的 FDM 打印机兼容。这项工作仍在进行中，但已经增加了对 Slic3r 和 [Prusa Slicer](https://hackaday.com/2019/05/24/3d-printering-the-past-and-future-of-prusas-slicer/) 的支持。我们期待看到它如何发展并被采用。