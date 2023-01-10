# 那些廉价雷达模块的频率如何？

> 原文：<https://hackaday.com/2022/12/06/how-on-frequency-are-those-cheap-radar-modules/>

如果你偏爱浏览全球速卖通、邦古德或易贝的不寻常的硬件，你可能已经看到了 HB100 多普勒雷达模块。这是一个 PCB，板上有一个金属罐，背面有一个贴片天线阵列。他们工作在 10.525 GHz 的频率上，[OH2FTG] [已经描述了其中几个的特征，以查看它们与该数字](https://www.youtube.com/watch?v=C5xWcHKanUE)有多接近。

这些器件有[一个表面上非常简单的电路](https://www.youtube.com/watch?v=TntNTVNq2Qc)，它大量使用 PCB 布局来创建微波电感、电容和调谐电路。有一个 FET 振荡器和一个二极管混频器，以及一个耦合 FET 输出和输入电感的介质谐振器。该组件提供频率稳定性，但其确切频率取决于其电场内的内容。因此，屏蔽不仅仅是屏蔽，而且对振荡器的频率和稳定性有显著影响。

较高质量的 HB100s 在罐的顶部有一个小调谐螺钉，它反过来调节频率。这应该在工厂里调整到正确的点上，但是在便宜的例子中经常没有。在这种情况下，他有一堆模块，虽然令人惊讶的是有些模块非常接近，但也有一些异常值位于很远的地方。

如果你使用 HB100，那么很可能没有人会打扰你，因为它的功率输出很小。但是，了解它们的内部工作方式以及在需要时如何调整它们是值得的。同时，如果你对多普勒雷达感兴趣，[以下是如何设计一个低频雷达](https://hackaday.com/2019/05/31/a-doppler-radar-module-from-first-principles/)。

 [https://www.youtube.com/embed/C5xWcHKanUE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/C5xWcHKanUE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

