# Mechpen: SCARA 绘画机器人

> 原文：<https://hackaday.com/2019/09/04/mechpen-scara-drawbot-for-the-big-picture/>

发现我们在纸上涂鸦是为了帮助思考、娱乐，或者仅仅是因为我们无聊，这并不罕见。但是，这种体力劳动是上个世纪才有的。现在是 2019 年，我们应该让机器人用交叉影线插图来填充我们的笔记本。在这一点上，【亚历克斯·韦伯】走在了我们的前面:他创造的[杰出的 SCARA 绘图机器人](https://tinkerlog.com/2019/08/27/mechpen/)可以在他的指挥下绘制各种各样的东西。

该机器人名为 Mechpen，发音为“McPen”，采用 SCARA(选择性柔顺装配机器人手臂)设计，两个平行轴控制手臂的 x-y 运动。机器人设计永远是一系列的取舍；在这种情况下，[Alex]牺牲了一些准确性来实现长距离。两个 NEMA 23 步进电机驻留在基地，随着所有的电子设备。这使得底座重达 15 公斤，这很好，因为它有助于在运动中稳定手臂。该手臂混合使用现成的和定制的硬件，其中大部分都布满了钻孔，以减轻移动部件的质量。由碳纤维管制成的两个 700 毫米的手臂部分使这个机器人能够达到 140 厘米的范围——足够用它漂亮的机械涂鸦填满一张 A0 纸。

手臂后面的大脑是两层的。为 3D 打印机设计的 Einsy RAMBo 板控制步进电机。除此之外，一个树莓派运行 Octoprint 来控制机器人。事实证明，这种选择对于解决机械问题非常方便:肘部在 Z 轴上弯曲得太厉害。肘部在 90 度与 180 度之间的笔高度差为 20-25mm；仅仅用一支弹簧笔解决太多的问题。解决方案是:使用为 3D 打印机设计的调平算法。VL6180X 距离传感器测量许多网格点到纸张的距离，然后软件在绘图时相应地上下移动伺服系统，以使笔保持在纸张上。

一些自定义编写的软件将 SVG 图形文件转换为适合打印的 gcode，允许选择不同的笔画和填充类型，并将不同的颜色分离为单独的 gcode 文件，以便用不同的笔绘制。

休息之后，一定要看看 Mechpen 的视频。

 [https://www.youtube.com/embed/xXfjJ8UWGWk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xXfjJ8UWGWk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们已经看到了这些部分的绘图机器人，比如[这个基于 pi 的绘图机器人非常适合在墙上绘图](https://hackaday.com/2018/10/08/another-drawbot-uses-a-pi-and-web-sockets/)。