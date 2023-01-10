# 工具从 KiCAD 生成交互式 PCB 图

> 原文：<https://hackaday.com/2021/08/03/tool-generates-interactive-pcb-diagrams-from-kicad/>

几乎每个人都喜欢漂亮的引脚排列图，但是涉及的引脚和功能越多，图就越混乱，越没用。为了解决这个问题，[Jan Mrázek] [创造了 *Pinion* ，这是一个帮助从 KiCad 设计文件](https://blog.honzamrazek.cz/2021/06/making-nice-looking-and-interactive-diagrams-for-your-pcbs/)生成交互式图表的工具。

结果是可以在任何 web 浏览器中查看的交互式图表。将鼠标悬停在管脚或焊盘上可以高亮显示那些带有名称标注的信号，单击可以使其保持高亮显示，以便于参考。进一步的信息可以根据需要或详细或简要。

有趣的是，Pinion *不是依赖于任何后端的 web 服务。这些图表只是静态的 HTML 和 JavaScript，很容易包含在网页中或嵌入到 GitHub 文档中。*

如果你觉得 Pinion 看起来有点眼熟，[你可能还记得我们曾介绍过[Jan]更早的 PcbDraw 工具](https://hackaday.com/2017/04/17/a-tool-for-kicad-board-renderings/)，它将 KiCad 电路板文件转换成 SVG 渲染，但没有添加标签或交互性的能力。Pinion 是这一早期思想的发展，它的图表可以作为文档和交互参考，不依赖任何外部服务。

感兴趣吗？ [Pinion 有完整的教程和演示](https://yaqwsx.github.io/Pinion/)以及不断增长的零件库，请查看。