# CoreFreq 给出了 Linux 上 CPU 性能信息的一瞥

> 原文：<https://hackaday.com/2022/12/24/corefreq-gives-peek-at-cpu-performance-info-on-linux/>

中央处理器是计算机的一部分，它使其他一切运转正常。虽然 GPU 越来越成为整体系统性能的关键部分，但我们仍然想知道我们的 CPU 做得如何。CoreFreq 是一个 Linux 工具,旨在告诉你你想知道的关于现代 64 位 CPU 的一切。

该工具依赖于一个内核模块，主要用 C 语言编写，一些汇编代码用于尽可能精确地测量性能。它能够报告从核心频率到超线程和睿频加速操作细节的所有信息。其他性能报告包括每周期指令数或每秒指令数的信息，当然还有您可能需要的所有热监控数据。这一切都在终端运行，有助于降低管理费用。

我们中的中坚分子可以从源代码构建它，可以在 [GitHub](https://github.com/cyring/CoreFreq) 上获得，尽管据报道它以包的形式提供，也可以作为现场 CD。我们可以想象从 CoreFreq 获取的数据也可以用于[一些有趣的性能可视化。](https://hackaday.com/2020/10/04/an-led-cube-to-display-cpu-vitals/)如果你一直在开发自己的漂亮的命令行工具，请务必[给我们写信！](http://hackaday.com/submit-a-tip)