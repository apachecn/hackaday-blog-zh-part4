# 一种超快速轻量无损压缩算法

> 原文：<https://hackaday.com/2021/11/30/a-super-speedy-lightweight-lossless-compression-algorithm/>

[Dominic Szablewski]在对 RGB 图像进行压缩时，他偶然想到了如何制作一种简单的无损压缩算法，从而产生了[非常好的图像格式](https://phoboslab.org/log/2021/11/qoi-fast-lossless-image-compression)，它似乎提供了与 PNG 格式相当的文件大小，但它非常简单，压缩速度快 50 倍，解压缩速度快 4 倍。用一个[微型的 300 行 C](https://github.com/phoboslab/qoi) 就可以实现。需要更多真实世界性能的细节吗？[Dominic]也谈到了这一点，提供了一套完整的[基准](https://phoboslab.org/files/qoibench/)供您阅读。

图像格式是这些天来由财团设计的东西之一，太多的复杂性使得它很难用有限的资源来实现，所以我们发现看到有人回归基础，制作一些超级轻量级的东西，并且在实用方面足够好，这非常令人耳目一新。

该算法的其他用途可以是超级简单的视频压缩，用于资源紧张的应用，并且一些低努力的带宽减少将是有益的。在小型 FPGA 中实现也很简单，因为对存储器的要求也很低。

该项目非常新，已经对格式进行了一些调整，因此 GitHub 项目代码可能会在没有警告的情况下进行更改，以反映[Dominic]认为必要的任何更正。

谢谢[大卫]的提示！