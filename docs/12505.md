# 不同地解析 png

> 原文：<https://hackaday.com/2022/01/17/parsing-pngs-differently/>

从我们的桌面应用程序到厨房里的电器，我们周围有数以百万计的小虫子。导致意外输出和行为的隐藏的任意条件。有很多方法可以找到这些错误，但是有一种方法我们很少听说，那就是在自己的代码中找到一个错误，却发现其他人也犯了同样的错误。例如，[大卫·布坎南]在他的[多线程 PNG 解码器中发现了一个 bug，并意识到苹果 PNG 解码器也有同样的 bug](https://www.da.vidbuchanan.co.uk/widgets/pngdiff/) 。

PNG(可移植网络图形)是一种[图像格式](https://en.wikipedia.org/wiki/Portable_Network_Graphics)，就像 JPEG、WEBP 或 TIFF 一样，旨在取代 gif。在头之后，文件的其余部分完全是块。每个块前面都有一个四个字母的标识符，有几个块是关键块。基本部分是 IHDR(头)，IDAT(实际的图像数据)，PLTE(调色板信息)，和 IEND(文件中的最后一块)。压缩是通过 zlib 中使用的 [DEFLATE](https://en.wikipedia.org/wiki/Deflate) 方法实现的，这本身就是串行的。如果你感兴趣，这里有一张来自[的关于格式](https://hackaday.com/2017/04/07/file-format-posters/)的[海报，这是我们前阵子讨论过的一个很好的资源](https://github.com/corkami/pics/blob/master/binary/PNG.png)。

鉴于 DEFLATE 本质上是串行的，恰当地格式化数据是很棘手的。[David]添加了称为 pLLD 部分的特殊部分(小写的第一个字母意味着它可以被不支持它的解码器安全地忽略)。这些部分让解码器知道给定的 IDAT 块可以安全地并行反序列化为 x 个块。苹果对其 iDOT 块使用了类似的技巧。然而，这里有一个问题。解压(a+b)是有可能的！=解压缩(a) +解压缩(b)如果 a 在非压缩块中途结束。由于 DEFLATE 方法使用窗口，将两个部分连接在一起会产生不同的结果。

由于现在对一个给定的 PNG 有两种可能的解释，你可以制作一个 PNG，当串行解码时，它显示一个图像，当并行解码时，它显示另一个图像。此外，[David]在桌面 safari 中发现了一个竞争条件，导致每次解码的图像略有不同。这是每一帧被解码的 PNG:

【David】在 GitHub 上写了[一个小工具](https://github.com/DavidBuchanan314/ambiguous-png-packer)把两张图片打包成一个 PNG。这让我们想起了[古老的隐写术，秘密数据隐藏在图像中。](https://hackaday.com/2012/02/27/this-image-contains-a-hidden-audio-track/)

(标题图片由[PawelDecowski]提供)。