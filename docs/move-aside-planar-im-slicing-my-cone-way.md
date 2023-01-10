# 让开平面，我在切我的圆锥体

> 原文：<https://hackaday.com/2022/11/21/move-aside-planar-im-slicing-my-cone-way/>

撇开佛利伍麦克乐队的双关语不谈，在过去的 30 年里，我们如何为打印机“切片”模型几乎没有什么变化。然而，CNC Kitchen [的 Stefan Hermann 有一个演示，试图通过圆锥形切片](https://www.cnckitchen.com/blog/guide-how-to-use-conical-slicing)来改变这一切。

对于第三维印刷黑暗艺术的门外汉来说，非圆锥切片的规范定义是以层高间隔将模型一分为二，生成周长和填充，然后将其作为 g 代码输出。这在数学上很容易实现，而且效果相当好，除非你在大多数打印机上有超过 60 度的突出部分。在圆锥形而不是平面上切片的[想法并不完全新颖，因为我们](https://www.cnckitchen.com/blog/conical-slicing-a-different-angle-of-3d-printing)[以前报道过 RotBot](https://hackaday.com/2022/10/09/rotbot-adds-a-extra-dimension-to-3d-printing-with-a-twist/) ，它提供了垂直旋转轴和 45 度角的打印头。不同寻常的是[Stefan]带你体验的技术是用普通打印机完成的，没有复杂的 45 度倾斜，是软件修改而不是硬件调整。

[Stefan]引用了 ZHAW 工程学院的[Michael Wüthrich]所做的早期工作，他写了一些应用该变换的脚本。切片器是 [SuperSlicer，](https://github.com/supermerill/SuperSlicer)PrusaSlicer 的一个分支，本身就是 slic3r 的一个分支。修改后的 g 代码将被导出，并可发送至您选择的打印机。他甚至有一个[链接，链接到一个预先切片的模型来试用](https://www.printables.com/model/315702-supportless-pipe-conical-slicing)。

当然，不同的打印机有不同的间隙水平，但他使用的 Prusa Mini 在传感器向上推的情况下有 16 度的间隙。[代码在 GitHub](https://github.com/CNCKitchen/ConicalSlicer) 上。注意到所有这些技术和分支是如何相互作用和建立起来的是很有趣的。无论倾斜切片、锥形切片还是其他什么最终成为事实上的标准，我们都期待更多的切片选择。

休息后的视频。

 [https://www.youtube.com/embed/1i-1TEdByZY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1i-1TEdByZY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

