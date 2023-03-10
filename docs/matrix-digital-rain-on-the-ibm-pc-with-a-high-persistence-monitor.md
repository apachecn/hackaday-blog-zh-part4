# IBM PC 上的 Matrix Digital Rain 具有高持久性监视器

> 原文：<https://hackaday.com/2022/01/03/matrix-digital-rain-on-the-ibm-pc-with-a-high-persistence-monitor/>

除非你在过去的 20 多年里一直躲在石头下面，否则你会遇到《黑客帝国》系列电影，以及经常使用的凉爽的绿色“数字雨”效果。这启发了[Oli Wright]想知道如果不是在现代显示器上运行动画，而是使用数字制作的磷光体余辉效果，而是在[一些复古的 PC 硬件上实现，使用实际的高余辉磷光体绿色单色显示器](https://www.youtube.com/watch?v=F7nSAEbJGLo)，会是什么样子。(视频嵌入，如下)幸运的是，[Oli]拥有一台 40 岁的 [IBM PC 5150](https://en.wikipedia.org/wiki/IBM_Personal_Computer) 以及与之匹配的 [IBM 5151 显示器](https://en.wikipedia.org/wiki/IBM_5151)，因此在 8088 汇编程序中实现这种效果以创建字符的下降序列是一件简单的事情。最终二进制少于 256 字节！

IBM 5151 的长显示持续时间旨在减少由于低扫描速率导致的显示闪烁的可见性，但当图像改变时，会产生令人讨厌的拖尾副作用。这正是[奥利]需要实现的效果，我们认为它看起来非常好。

[Oli]利用由[Jeff Parsons]编写的优秀的[PCjs 基于浏览器的仿真器](https://www.pcjs.org/software/pcjs/)来演示软件正在做什么，而效果并不明显。如果你愿意，你可以自己尝试一下，因为在[项目 GitHub](https://github.com/OliWright/digirain/blob/main/digirain.asm) 上可以找到组装列表。

当然，我们已经讨论了很多数字雨的效果。以前很多次，例如，用[这个 Arduino 库](https://hackaday.com/2021/11/17/arduino-library-makes-digital-rain-like-its-1999/)，这里有一个[定制的 PC 机箱侧面板](https://hackaday.com/2021/12/28/enter-the-matrix-with-this-custom-pc-side-panel/)早在 2021 年 12 月，如果你还记得那些日子的话。

 [https://www.youtube.com/embed/F7nSAEbJGLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/F7nSAEbJGLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

