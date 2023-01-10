# TI 和 Cadence 让 PSpice 免费

> 原文：<https://hackaday.com/2020/09/20/ti-and-cadence-make-pspice-free/>

我们喜欢模拟软件。德州仪器长期以来一直提供 TINA，但最近他们与 Cadence 合作，在有一些限制的情况下免费提供 [OrCAD PSpice。你可能听说过 PSpice——它广泛应用于学术界和工业界，但通常非常昂贵。您可以在下面看到一个促销概述视频。](https://e2e.ti.com/blogs_/b/analogwire/archive/2020/09/14/how-to-simulate-complex-analog-power-and-signal-chain-circuits-with-pspice-for-ti)

该计划需要注册和批准步骤才能获得许可证密钥。下载的程序有 TI 模型和其他标准模型。只要坚持使用提供的库，似乎没有什么限制。根据[数据表](https://resources.orcad.com/pspice-for-ti/pspice-for-ti-datasheet&utm_medium=app&utm_campaign=pspiceti)，在这种情况下没有尺寸或模拟复杂度限制。如果您想使用其他模型，您可以这样做，但这正是您受到限制的地方:

> 设计中可以导入多少第三方模型没有限制。但是，如果导入第三方模型，当从网络导入任何第三方模型时，用户一次最多可以选择绘制 3 个信号。

我们并不完全确定“来自网络”是什么意思，但可以推测他们只是指来自其他来源。无论如何，您仍然可以获得交流、DC 和瞬态分析，以及大量选项，如最差情况时序分析。如您所料，它支持混合信号设计，并提供丰富的数据绘图选项。

这是一个很好的机会来驱动一些在行业中广泛使用的严肃软件。唯一让我们失望的是？它在 Windows 下运行。我们无法让它在 Wine 下工作，但 Windows 10 虚拟机处理得很好，尽管我们真的讨厌在没有必要的情况下运行虚拟机。

尽管如此，价格是正确的，这是一个伟大的软件。我们也喜欢最近的 [Micro-Cap 12](https://hackaday.com/2020/01/08/commercial-circuit-simulator-goes-free/) 版本，但我们不期待任何更新。当然， [LTSpice](https://hackaday.com/2016/02/26/adding-spice-to-your-workbench/) 也是相当能干的。

 [https://www.youtube.com/embed/7CLHTBKI9-w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7CLHTBKI9-w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

