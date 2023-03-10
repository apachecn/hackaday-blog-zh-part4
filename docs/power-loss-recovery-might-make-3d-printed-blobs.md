# 断电恢复可能会产生 3D 打印斑点

> 原文：<https://hackaday.com/2022/10/10/power-loss-recovery-might-make-3d-printed-blobs/>

[怪胎绕道]有一个谜要解开。他正在打印的一个圆形零件上有清晰的斑点图案。如果你从事 3D 打印已经有一段时间了，你应该知道打印中的停顿会导致像这样的斑点。他还展示了同一部分的完美打印版本，并声称它来自同一台打印机，使用相同的材料，甚至切片器设置。那么是什么导致了这些斑点呢？你可以在下面的视频中找到答案。

但是，正如您从标题中可能猜到的那样，问题是打印机内置的掉电恢复功能。虽然视频中有很多内容，但你可以将其分解为几个项目，所有这些都可以用一种或另一种方法解决，包括简单的解决方法:关闭掉电恢复。

如果您从未使用过具有断电恢复功能的打印机，那么它的目的是让您在断电时可以继续打印作业。为此，打印机会定期向 SD 卡写入一些状态信息。如果您的 SD 卡运行缓慢，或者您试图从同一个 SD 卡打印，则可能会引发此问题。但事实远不止如此。

第一个问题是，像这样光滑的圆形物体往往会产生大量的 gcode。您可以用几种方法来控制这一点，包括在设计时和通过设置切片的分辨率。此外，您可以确保您的固件支持电弧，并指示您的切片机发射电弧或使用名为 arc welder 的 Octoprint 插件。这可以显著减少这些弧中涉及的 gcode 数量。

另一种可能性是增加固件中的缓冲区。如果你能重建马林，这并不难做到。问题是，使用掉电功能也是捆绑 SD 卡，所以你可以提前读取的越多，它就有越多的时间写入卡中以掉电。顺便说一下，有一个名为 [Buffer Buddy](https://github.com/chendo/BufferBuddy) 的 Octoprint 插件，它可以让你深入了解你的打印问题，尽管它也可以挂起你的打印机，特别是——我们发现——如果你也启用了 Meatpack 来压缩串行上的 gcode。即使你不想安装它，关于为什么曲线有时会导致斑点的讨论在自述文件中也有很好的解释，更不用说[相关的博客帖子](https://chen.do/mitigating-print-quality-issues-with-bufferbuddy/)。

我们也对[极客绕道]的延时视频印象深刻，这些视频相当电影化，使用了运动控制摄像机。如果你想了解更多关于[电弧焊](https://hackaday.com/2020/11/03/this-gcode-post-processor-squeezes-lines-into-arcs/)(3D 打印机那种，不是火花和金属那种)，我们之前已经谈过了。如果你想知道更多关于制作 3D 照片的[延时，我们也已经报道过了。](https://hackaday.com/2018/07/02/coolest-way-to-watch-3d-printing-lights-camera-octolapse/)

 [https://www.youtube.com/embed/ZM1MYbsC5Aw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZM1MYbsC5Aw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

