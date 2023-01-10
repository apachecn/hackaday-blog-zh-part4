# xilinx 的红外滤光片

> 原文：<https://hackaday.com/2021/05/18/fir-filters-for-xilinx/>

数字滤波器总是一个有趣的话题，对于 FPGAs 来说尤其具有吸引力。[Pabolo]在一系列博客文章中与他们合作。[最新的](https://www.controlpaths.com/2021/05/17/implementing-a-fir-filter-using-folding/)涵盖了 Verilog 中的一个 8 阶 FIR 滤波器。他讲述了一些数学知识，这些知识在很多地方都可以找到，但他也展示了实现如何映射到器件中的 DSP 片。然后为了减少切片的数量，他举例说明了用延迟时间换取切片使用的折叠。

折叠采用多级并行乘法，并将其分解为在较长时间内完成的较少乘法。这可以重用切片来减少高阶滤波器所需的数量。

最后，您可以看到同一个滤波器的三种不同实现，这很好地说明了每种实现是如何使用资源、功耗和时间的。代码都可以在 [GitHub](https://github.com/controlpaths/blog) 上找到。这些帖子主要关注 Xilinx，但也有对其他 DSP 模块风格的讨论。

数学上，FIR 滤波器没有极点，这意味着它总是稳定的。然而，与使用状态信息的 IIR 滤波器相比，它们需要更高的滤波器阶数才能获得类似的性能。

如果你想玩 FIR 滤波，你可以做一些模拟。或者你可以[使用电子表格](https://hackaday.com/2019/10/03/dsp-spreadsheet-fir-filtering/)。