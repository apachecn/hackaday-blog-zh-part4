# 通过草图更好地编码

> 原文：<https://hackaday.com/2022/12/03/better-coding-through-sketching/>

早在 20 世纪 70 年代末和 80 年代初，工程专业的学生会花几个学期的时间进行制图，通常会有一两周的“计算机辅助制图”在那个时候，这意味着在卡片上打出矩形 20，30 或类似的数字，然后在绘图仪上得到结果。然后我们转向了图形 CAD 软件包，但是最近，一些软件又回到了描述而不是绘制复杂的设计。康奈尔大学的研究人员正试图为编码提供同样的选择。他们已经建立了一个叫做 [Notate](https://techxplore.com/news/2022-11-tool-code.html) 的 Juypter 笔记本扩展，允许你勾画和手写与传统计算机代码交互的程序部分。下面可以看到一个关于作品的视频。

这个例子展示了量子计算，但是这个想法可以应用于任何事情。这个例子有生成量子电路的草图。自然有机器学习的参与。

我们不否认这是一个很好的选择，但当涉及到 FPGAs 时，我们学到了想要绘制的教训。当你启动 FPGAs 时，有一种倾向是想画原理图，跳过 VHDL 或 Verilog 之类的高级语言。但如果在原理图中使用 7 段解码器，就很难画出来，而且容易出现难以纠正的错误。但在 VHDL 或 Verilog 中，它是几行可读性高、可修改性强的代码。现在试着用原理图设计一个 CPU。这是可以做到的，但需要做更多的工作。

通常，当你听说图形化编程时，它是[更结构化一点的](https://hackaday.com/2019/01/09/mit-scratch-3-0-opens-new-doors-for-users-and-builders-alike/)。我们想知道 Notate 将如何处理[草书](https://hackaday.com/2022/10/06/immersive-cursive-growing-up-loopy/)？

 [https://www.youtube.com/embed/Eynks13Gsfg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Eynks13Gsfg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

