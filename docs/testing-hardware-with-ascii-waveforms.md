# 用 ASCII 波形测试硬件

> 原文：<https://hackaday.com/2020/06/06/testing-hardware-with-ascii-waveforms/>

测试软件有时比测试硬件更容易。毕竟，在使用通用工具监控输出之前，您总是可以创建测试文件，甚至伪造用户输入。不过，硬件有点不同。有时候很难想象到底发生了什么。[安德鲁·雷的]回答？[使用 ASCII 文本](https://blog.janestreet.com/using-ascii-waveforms-to-test-hardware-designs/)产生模拟波形。

这个过程使用了一些用 OCaml 编写的定制工具，但是代码可以在 [GitHub](https://github.com/janestreet?q=expect&type=&language=) 上找到。这款名为 [Hardcaml](https://github.com/janestreet?q=hardcaml&type=&language=) 的工具允许你为硬件编写测试平台——这对于 FPGA 开发者来说并不是一个新想法。然而，输出是一个 ASCII 文本波形，常用的软件开发工具可以对照预期的输出来检查该波形。

当然，你可以用 Verilog VCD 文件做同样的事情，但是读起来就没那么有趣了。你需要使用波形查看器来真正了解发生了什么。事实上，我们想知道是否值得走另一条路，将 Hardcaml 输出转换为 VCD，以便您用来区分波形的工具可能会工作。

我们喜欢 [ASCII 艺术](https://hackaday.com/2016/06/28/retrotechtacular-ascii-art-in-the-19th-century/)。事实上，我们早在 2002 年就在 [ASCII CAD](http://www.al-williams.com/free/asciicad.htm) 进行了自己的尝试。如果你愿意，你甚至可以带着你的 ASCII 艺术作品去 [3D。](https://hackaday.com/2020/01/01/explore-this-3d-world-rendered-in-ascii-art/)