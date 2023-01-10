# 用 PDFrankenstein 注释 Linux 上的 pdf

> 原文：<https://hackaday.com/2022/05/28/annotate-pdfs-on-linux-with-pdfrankenstein/>

在 Windows 和 Mac 机器上，在 PDF 文件中添加文本或绘图(如签名)并不太麻烦，但【Mansour Behabadi】发现，在 Linux 机器上，似乎并没有一种令人满意的方式或简单的工具。作为一名有事业心的黑客，[Mansour] [开始填补这个空白](https://blog.oxplot.com/annotate-pdfs-on-linux/)，它在幕后的工作方式确实令人愉快。

阻碍创建这样一个工具的主要因素是 PDF 格式是一个复杂和扭曲的东西。制作一个能够插入超链接、注释、图像或绘图的通用 PDF 编辑工具并不是一个周末项目。但是[曼苏尔]没有让这阻止他；他利用了 Linux 上已经存在的可以读取和创建 PDF 文件的工具这一事实，并将它们捆绑在一起，形成了一度被称为“可怕的工具大杂烩”的东西，由此产生了 [pdfrankenstein](https://github.com/oxplot/pdfrankenstein) 这个名字。

该工具是一个 GUI，使用 [Inkscape](https://inkscape.org/) 和 [qpdf](https://github.com/qpdf/qpdf) 将 pdf 页面转换为 SVG 文件，将其设置为锁定的背景，然后让用户使用 Inkscape 作为编辑器添加他们想要的任何注释。更改完成后，程序会移除背景，将注释覆盖到原始文件上，并导出最终文件。因此，注释可以是在 Inkscape 中可以完成的任何事情。

对这些和其他处理 pdf 的工具感到好奇吗？当我们之前讨论在 Linux 中处理 PDF 格式时，我们已经分享了一些程序和技巧。