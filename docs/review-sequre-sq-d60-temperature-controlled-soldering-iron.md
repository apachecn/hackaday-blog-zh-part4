# 回顾:Sequre SQ-D60 温控烙铁

> 原文：<https://hackaday.com/2021/04/27/review-sequre-sq-d60-temperature-controlled-soldering-iron/>

在过去的几年中，一种新型的烙铁出现了:一种温控烙铁，不再依赖于庞大的电源供电的基站，而是使用低压 DC 电源，所有的电子设备都隐藏在一个细长的手柄中。首先是迷你软件 TS100，然后是更多，功能略有不同，价格也各不相同。这些年来我们已经回顾了其中的一些，今天我们有了最新的竞争者 SQ-D60。它严格遵循配方，但只需 20 英镑(约 26 美元)。这个价格使它成为一个有吸引力的预算类别，它的 USB-C 电源选项使它比带桶形插孔的型号更具前瞻性。描述结束了，是时候插上电源，测试一下了。

## 盒子里有什么？

[![That's a lot of extra bits for a budget iron!](img/c69cc56ee252af6ba3cf67de5e8461e6.png)](https://hackaday.com/wp-content/uploads/2021/03/sequre-d60-parts.jpg)

That’s a lot of extra bits for a budget iron!

在盒子里，除了包含电子设备的手柄之外，还有一系列令人惊讶的零件和附件。手柄本身的大小与其竞争对手类似，只是比 Pine64 的 Pinecil 稍长一点。提供的齿尖出乎意料地是一个倾斜的凿子，所以我可能订购错误，尽管由于它与 TS100 和 Pinecil 具有相同的齿尖设计，如果需要的话，我还有很多可供选择的齿尖。此外，还有一小袋六角螺钉以及一把钥匙和一个驱动器，一个小海绵支架，一套 Sequre 贴纸，一根 USB-C 到桶形插孔电缆，以及一个用于 LiPo 电池组的桶形插孔到 XT60 连接器。这最后两条电缆是一个特别有用的补充。

乍一看，尖端似乎没有任何固定在其插座中的方法，但仔细观察会发现，在硅胶指套下隐藏着一个六角螺钉，当拧紧时，它会牢牢地固定住它。手柄有一个足够简单的界面，只有两个按钮和一个 3 位 7 段显示屏。从 45 W 的 USB-PD 电源给它供电，按下其中一个按钮后，它在大约 10 秒钟内加热到 300°C。我通常的焊接温度是 360°C，它有一个界面，涉及长按其中一个按钮，然后它们变成上下按钮来选择温度。在长时间的使用中，手柄并没有明显变暖，除了轻微的新电子产品变热的气味，也没有立即担心它可能会释放出神奇的烟雾。

## 像其他几个熨斗一样

[![As far as I could dismantle the iron.](img/45bafd4130330cca30d347987719001e.png)](https://hackaday.com/wp-content/uploads/2021/03/sequre-d60-in-pieces.jpg)

This is as much dismantling as I could do, those silicone buttons were the undoing of the effort.

在使用中，它与我们见过的其他类似大小和形状的熨斗非常相似。焊接很简单，它很轻，易于使用，热量充足。说明书上有一张内部结构的放大图，但我很痛苦地承认，这个熨斗提供了一个罕见的时刻，让我的拆卸技能失败了。出乎意料的是，尖端安装在一个子组件上，该子组件使用 3.5 毫米的插孔远离主板，虽然这很容易移除，但事实证明几乎不可能将主板滑出手柄管。原因是两个硅胶按钮会粘在显示屏上，尽管哄了很久也不动。我可以通过故意破坏按钮或显示器来暴露电路板，但因为我更喜欢让熨斗有用，所以我没有这样做。如果有类似的熨斗，我希望它包含一个 USB-PD 芯片，一个 8 位微控制器，因为它没有 TS100 或 Pinecil 的固件可升级功能，然后是一个 MOSFET 来控制尖端。这是这些熨斗的可靠配方。

该不该买一个？如果你正在寻找一个功能合理的迷你熨斗和一些真正有用的电缆捆绑在一起的预算价格，是的。它不像我们去年初审查的超预算[SanErYiGo SH72](https://hackaday.com/2020/01/27/review-saneryigo-sh72-soldering-iron/)那么便宜，但与那台熨斗不同的是，它有数字控制和 USB-C。将它与旧的可靠的[ts 100](https://hackaday.com/2017/07/24/review-ts100-soldering-iron/)和超级黑客的[Pinecil](https://hackaday.com/2021/01/05/review-pine64-pinecil-soldering-iron/)进行比较，并做出自己的决定。