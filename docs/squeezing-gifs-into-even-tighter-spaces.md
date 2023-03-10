# 将 gif 压缩到更小的空间

> 原文：<https://hackaday.com/2022/12/21/squeezing-gifs-into-even-tighter-spaces/>

使用小型 AVR 微控制器在 TFT 或有机发光二极管显示器上显示图像是一项挑战，因为它需要大量的存储空间。一种解决方案是压缩图像，但是你需要更多的内存来解压缩，这是另一个问题。 *Technoblogy* 的【戴维·约翰逊-戴维斯】找不到符合他需求的 GIF 解码器，所以[开始编写自己的](http://www.technoblogy.com/show?45YI)。

我们之前已经看到了针对 Cortex-M0+的最小 GIF 解码，它需要 24 K 的内存，但是这项技术运行在只有 12 K 内存的 AVR 上。在这个过程中，[David]使用一些小技巧来削减需求。由于他的目标 TFT 是一个 5-6-5 颜色空间，这些 3 字节的颜色变成了 2 字节。LZW 查找表被编码为指向较早条目的 12 位指针加上一个附加像素。然而，这些节省是有代价的。不支持动画、本地颜色表、透明度、交错或 GIF87a 格式的图像。但是他把它移植到了 PyBadge 上，py badge 是基于 AMD51 的。

[David]提供了一些示例代码来显示来自程序内存和 SD 卡的 GIF。所有的[代码都在 GitHub](https://github.com/technoblogy/minimal-gif-decoder) 的 CC By 4.0 许可下。