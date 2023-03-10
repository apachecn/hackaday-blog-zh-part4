# 一个开源工具来记录您的布线

> 原文：<https://hackaday.com/2020/06/23/an-open-source-tool-to-document-your-wiring/>

我们大多数人都熟悉用于制作电路图的工具，因为这通常是制作定制 PCB 的第一步。但是，那些不在主板上的电缆和线束呢？你如何轻松地记录你最新最伟大的创造的完美逻辑线路？

这正是导致[丹尼尔·罗哈斯]创建 wire viz 的问题。这个开源 Python 工具获取人类可读的输入文件，并将它们转换成有吸引力的功能性可视化图形，显示项目中所有线路的走向。它甚至可以用来生成材料清单，记录连接所有东西所需的电线长度和连接器类型。

如果您仍然使用预制电缆将所有组件连接在一起，那么您可能不会立即看到这种工具的好处。[但是正如我们过去讨论过的](https://hackaday.com/2018/10/19/bradley-gawthrop-loves-wiring-and-so-should-you/)，创建定制线束是严肃的硬件黑客应该熟悉的事情。是的，这需要更多的努力，但最终结果是值得的。有了像 WireViz 这样的工具，为你的下一个项目创建一个定制的线束变得更加容易了。

[Daniel]在记录这个项目方面做得非常出色，[不仅提供了如何喂养和护理 WireViz 的教程](https://github.com/formatc1702/WireViz/blob/master/tutorial/readme.md)，还提供了一系列示例，展示了该工具可以帮助理解的[复杂布线。但是还有很多工作要做，他很高兴从任何想参与的人那里得到反馈或代码贡献。](https://github.com/formatc1702/WireViz/blob/master/examples/readme.md)