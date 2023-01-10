# 弯曲你的指纹以消除支撑

> 原文：<https://hackaday.com/2022/05/01/bend-your-prints-to-eliminate-supports/>

当设计一个相当简单的 3D 打印零件时，你需要考虑到它需要的所有支持。战略性的偏置、倒角和圆角是我们的工具箱中的必备工具。随着时间的推移，我们已经学会了调整我们的设置，这样，希望我们不必在床冷却后用 xacto 刀四处摸索。在 Twitter 上，Chris [展示了他的可折叠 3D 打印实验](https://twitter.com/signalskew/status/1519706021588967425) ( [nitter](https://nitter.net/signalskew/status/1519706021588967425) )通过将零件打印为一个单件，一旦你从床上弹出它，它就可以折叠成一个块，从而解决了支撑问题。

这个技巧的主要组成部分似乎是印刷品折叠处的形状，以及垂直于折叠线方向的底层线的排列。[Chris]展示了他的 FreeCad 设计的横截面，分享了他发现最有效的尺寸。

当然，这是 Twitter，所以其他黑客正在提出改进设计的建议——就像[这个可能会改善对齐的受控楔形物](https://twitter.com/MisterHW/status/1519759949949194240)的草图。至于层线方向对齐，[克里斯] [承认通过旋转切片机中的部分，直到层线的方向恰到好处。人们](https://twitter.com/SignalSkew/status/1519709107715981313)[已经对这个](https://twitter.com/jkbckr/status/1459228518416539663)进行了一段时间的实验，像这样的技巧总是我们工具箱中受欢迎的新成员。你可能想知道——这种铰链对什么样的项目有用？

【Chris 提供的例子是一个 Eurorack 铁路段——由于需要悬臂，您可能会倾向于垂直打印，这会影响打印时间并导致结构缺陷。有了这一招，你绝对不用！你还可以走得更远，3D 打印一个单片可折叠的[树莓皮零盒](https://twitter.com/stockholmux/status/1458897101899788299)，可打印的[，](https://www.printables.com/model/184727-print-flat-and-fold-case-for-raspberry-pi-zero-2-w)只需要两个额外的端盖就可以把它固定在一起。

可折叠 3D 打印并不新鲜，尽管我们通常看到它们是用技术上独立的[就地打印铰链](https://hackaday.com/2017/08/26/design-and-3d-print-robots-with-interactive-robogami/)完成的。这个技巧是避免支撑和任何碎片分离的根本解决方案。在激光切割中，我们已经知道类似的技术有一段时间了，称为[“活动铰链”](https://hackaday.com/2017/04/06/two-piece-boxes-thanks-to-laser-cut-flex-hinges/)，但我们通常没有将这种技术扩展到 3D 打印中，除了少数[制造级技术](https://hackaday.com/2018/11/04/living-hinges-at-the-next-level/)。像这样的铰链一般不会弯曲很多次才断裂。也有可能解决这个问题——上次我们谈到这个问题，这是一个[漫长的旅程，结合塑料和织物](https://hackaday.com/2021/07/27/see-this-hybrid-approach-to-folded-3d-printed-mechanisms/)来生产难以置信的小型 3D 打印机器人！

我们感谢【混沌】与我们分享这个！