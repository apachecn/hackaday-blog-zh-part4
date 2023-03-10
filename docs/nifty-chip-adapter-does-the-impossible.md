# 漂亮的芯片适配器做不可能的事

> 原文：<https://hackaday.com/2021/10/09/nifty-chip-adapter-does-the-impossible/>

半导体短缺减少了设计师的选择，导致一些创造性的解决方案被发现，但[djzc] 使用的[可能是我们见过的最具创造性的解决方案。今年，许多工程师陷入了“封装陷阱”( footprint trap ),即电路板是为一个封装设计的，但短缺意味着该器件只能在另一个封装中使用。在这种情况下，FTDI 芯片被设计成具有用于 QFN 封装的 PCB 足迹，而找到的唯一芯片是来自分线板的 QFP。](https://twitter.com/dzjc2/status/1441247634656665607)

[![The three boards which make up the adaptor](img/a6dc4016c088b921a1d972085fcc3979.png)](https://hackaday.com/wp-content/uploads/2021/09/qfn-to-qfp-boards.jpg)

The three boards which make up the adapter

对于那些不熟悉半导体封装的人来说，QFN 和 QFP 有着非常相似的环氧树脂封装，但 QFN 的引脚底面与环氧树脂齐平，而 QFP 的引脚向侧面张开。QFP 相对来说更容易手工焊接，所以我们在这些页面上看到的可能比 qfn 更多。

QFP 没有机会直接焊接到 QFN 的封装上，那该怎么办呢？解决方案是一个非常有创意的方案，一个桥接两者的双 PCB 夹层。下面的 PCB 由厚材料制成，并在周围元件的水平上方反映 QFN 足迹，而上面的 PCB 在其下侧具有 QFN，在其上部具有 QFP。当它们连接在一起时，它们形成一个倒置的大礼帽结构，下面是 QFN 足迹，上面是 QFP 足迹。很难焊接到位，但结果是芯片可以附着在 QFP 上。我们喜欢它，它比 [elite dead-bug 焊接](https://hackaday.com/2020/09/05/incredible-soldering-in-the-name-of-hardware-support/)优雅得多！