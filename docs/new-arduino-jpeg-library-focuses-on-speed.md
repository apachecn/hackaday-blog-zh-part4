# 新的 Arduino JPEG 库专注于速度

> 原文：<https://hackaday.com/2020/08/26/new-arduino-jpeg-library-focuses-on-speed/>

在微控制器上处理图形一直意味着专注于充分利用有限的资源。特别是在 8 位时代，各种各样的伎俩被用来让低性能芯片实现超越其卑微地位的壮举。然而，这些天来，我们有幸拥有 32 位的工作主机，时钟速度达到几十甚至几百 MHz，并有许多千字节的 RAM 与之匹配。在编写 JPEGDEC 库时，[Larry]考虑的就是这些更高性能的芯片。

[正如【Larry】在主题为](https://bitbanksoftware.blogspot.com/2020/08/optimizing-jpeg-decoding.html)的博客文章中所讨论的，Arduino 平台已经有 JPEG 库了。然而，其中许多是针对 8 位平台，内存很少。虽然在这种情况下，可以用一些智能代码一片一片地解码 JPEGs，但如果你有更多的空间，速度可能会快得多。自从 1994 年写了他的第一个 JPEG 解码器，在过去的 20 年里，他做了大量的工作来解释他开发的各种优化。从消除不必要的标记检查到忽略不需要的数据以缩小输出，所有这些都有助于更快地完成工作。该库的目标是 Cortex-M0+，或任何最小内存为 20K 的芯片，作为其最低运行要求。时钟频率更高的更快芯片自然表现更好，[Larry]使用该库为各种常见硬件提供了基准解码时间。

[在](https://hackaday.com/2020/08/03/optimizing-gif-playback-for-microcontrollers/)之前，我们已经展示了用于 Arduino 平台的【Larry】的 GIF 解码器，这也是一个为良好性能而优化的有用库。如果你有自己的在微控制器上处理图像的巧妙方法，[你知道如何调用！](http://hackaday.com/submit-a-tip)