# RGB 7 段显示模块发出各种颜色的光

> 原文：<https://hackaday.com/2022/06/19/rgb-7-segment-display-module-glows-in-all-the-colours/>

虽然 7 段显示器都很好，但它们现在被认为有点过时了。来自[Matt Deeds]的这个项目将他们带向尖叫的未来，尽管在彩虹下展示每一种颜色。

![](img/26f2a5c18fb5139a3eac5700bb6b3309.png)[Matt]的产品由一个 PCB 组成，PCB 上装有 SK6812 侧装 led，以典型的 7 段模式布局。每个 PCB 都有两个 7 段数字。SK6812 LEDs 的驱动方式与著名的 WS2812B 可寻址 led 相同，但它们的优势是在一系列电源电压下颜色和亮度更稳定。

随着 led 的安装，第二个 PCB 仅用作扩散器，省去部分阻焊膜，这是一个紧凑的 7 段解决方案，厚度仅为 2.7 毫米。额外的好处是，由于可寻址的 RGB LEDs 的性质，每个部分都可以设置为不同的颜色。在这方面做得太过火会使显示器难以阅读，但它可以用来轻松地显示绿色、红色或黄色数字，例如，创建一个数字范围的可视指南。

这是一个伟大的构建，我们喜欢看到 7 段显示器以不同的方式重新想象—[甚至是机械地！](https://hackaday.com/2021/11/13/a-one-servo-mechanical-seven-segment-display/)与不可寻址 LED 时代的旧方式相比，它还需要更少的引脚来驱动。如果你有自己的正在开发的 7 段项目，[请告诉我们](https://hackaday.com/submit-a-tip/)！