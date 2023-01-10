# 家酿曲线跟踪与大枪竞争

> 原文：<https://hackaday.com/2022/07/22/homebrew-curve-tracer-competes-with-the-big-guns/>

当我们第一次看到 VBA 曲线跟踪器时，我们认为它可能与 Visual Basic for Applications 有关。但事实证明，它是创作者的名字的大杂烩:[保罗·弗斯泰格]、[巴德·贝内特]和[马克·阿利]。[Paul]在 2017 年设计了一个原型。自那时以来，该项目不断发展，并吸取了经验教训。最终曲线描绘器在很多方面都给人留下了深刻的印象。

如果您从未使用过曲线跟踪器，它们允许您使用元件的电压-电流特性曲线来表征元件。你使用示波器作为输出设备。工程师经常使用这种仪器来理解或匹配二极管、晶体管等器件，有时甚至是电子管。例如，如果您想测量集电极-发射极击穿电压或集电极截止电流，这是您的首选器件。您还可以在重要的电路中匹配增益(例如，推挽电路，其中两个晶体管放大同一信号的不同部分)。

如果你想更多地了解它是如何工作的，有一系列博客帖子涵盖了该设备的演变。你也可以在 [GitHub](https://github.com/paulvee/VBA-Curve-Tracer) 上找到设计文件。这里还有一个便利的帖子，展示了你可能想要进行的多种类型的[测量。](https://www.paulvdiyblogs.net/2021/11/making-meassurements-with-v3-curve.html)

这是一个很好看的项目。我们已经看到它以便宜的价格完成，但是很慢。或者[花 15 美元，做得更好](https://hackaday.com/2016/07/22/super-in-depth-15-curve-tracer-project/)。我们怀疑这些都没有足够高的电压来做大多数电子管，但[他们在 20 世纪 50 年代为电子管制造了相同的基本仪器](https://hackaday.com/2020/04/20/tubes-have-character-with-a-tek-570/)。