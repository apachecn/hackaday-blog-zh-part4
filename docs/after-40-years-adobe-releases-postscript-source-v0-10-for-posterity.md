# 40 年后，Adobe 为后代发布 PostScript 源代码 V0.10

> 原文：<https://hackaday.com/2022/12/13/after-40-years-adobe-releases-postscript-source-v0-10-for-posterity/>

为了庆祝成立 40 周年， [Adobe 向计算机历史博物馆](https://computerhistory.org/blog/postscript-a-digital-printing-press/)发布了 PostScript v0.10 的源代码。但是在你问之前，我们已经试过了，它不能开箱即用地编译 GCC 它至少缺少了`except.h`,但是我们敢打赌，只要稍加努力，你就能破解它。

PostScript 是 PDF 的前身，在当时是革命性的。出自施乐的 PARC，其想法是创建与设备和分辨率无关的文档，其中所有的字符、符号和图形都用它们的形状而不是位图来描述。PostScript 的秘密在于它如何回到基于像素的表示，以最终用于显示器或打印机。毫不夸张地说，这最终彻底改变了印刷行业，这在 CHM 的收藏中是有意义的。

不过，在商业秘密方面，你不应该太兴奋。显然，这里发布的代码只包括 Adobe 字体提示算法的第一个草案版本，正如早期版本号所证明的那样。尽管如此，你可以自由地钻研可读性很好的 c 语言。例如，`vm.c`包含了实现 PostScript 的几乎类似 Forth 的语言的虚拟机。

当然，如果你只是喜欢摆弄 PostScript，下载一个像 [GhostScript](https://www.gnu.org/software/ghostscript/) 这样的现代开源解释器可能更有意义。即便如此，看到一切开始的原始代码库还是很有趣的。