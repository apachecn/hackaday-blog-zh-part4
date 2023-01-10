# 测量能源消耗

> 原文：<https://hackaday.com/2018/08/03/measuring-energy-consumption/>

您可能会认为测量许多复杂的交流功率参数，如有功和无功功率、均方根电压和电流以及线路频率，是一项繁重的工作。事实证明，在很多情况下，都有一个芯片。微芯片 MCP39F511 可以做到所有这些，但需要一些变压器的帮助。[Boris Landoni]有一篇由两部分组成的文章,不仅展示了这种用芯片制造的电表，还非常详细地描述了 IC 的操作及其工作原理。该设置需要两个变压器。一个用来降低电压，另一个用来测量电流。

也许只是我们，但是我们发现这两张图表有点混乱。上面有两个 ic 的原理图是带有 MCP39F511 的实际电路板(另一个 IC 是稳压器)。原理图上的变压器似乎只有一个 ic，U1，但事实并非如此。原理图上的 U1 是第一个原理图中的整个电路板。第二个原理图上的“IC”引脚编号是第一个原理图上的 CN2 引脚。除了 U1 是第一个原理图中的实际电路板之外，两张原理图中的 CN1 和 CN2 没有任何关系。

第二个帖子没有那么致命，因为它[涵盖了软件](https://www.open-electronics.org/energy-meter-module-to-analyze-the-electrical-grid-parameters-and-consumption-the-software-part-2/)，尽管不清楚实际上从哪里获得代码。然而，由于 MCP39F511 具有简单的寄存器结构，因此用您选择的语言读出测量参数应该没有任何问题。

如果您想了解电能计量的另一种方法，[我们已经看到了其他几个项目](https://hackaday.com/2016/05/25/meter-all-the-phases-three-phase-energy-meter-with-openwrt/)。显然，当你在用电源工作时，你需要[小心](https://hackaday.com/2016/05/11/looking-mains-voltage-in-the-eye-and-surviving-part-1/)。