# SMD 试验板适配器跳过原理图，直接连接到 PCB

> 原文：<https://hackaday.com/2020/10/17/smd-breadboard-adaptors-skip-schematic-goes-straight-to-pcb/>

如果您需要在面包板上的原型中添加一两个 SMT 芯片，Travis Hein 已经为您提供了承保服务。他使用 KiCad 为各种 SOIC、SOT23 和 DPAC 模式设计了一套小型 SMD 转接板。他已经将它们作为开放源代码发布，所以您可以随意使用或根据需要修改它们。

通常，我们不会看到有人在设计 PCB 时绕过原理图。但是我们可以同意[Travis]已经发现了一种直接进入 PCB 更有意义的情况。他只需将封装放入 Pcbnew 中，添加一些引脚接头，然后直接在 PCB 上布线。(但是不要担心，你们中的一些人可能还记得[Travis]早期的[SSR 电源开关项目](https://hackaday.com/2018/05/17/diy-ssr-for-mains-switching/)，这证明了他确实能画出正确的原理图。)我们知道有更多的人更喜欢直接进入 PCB 布局…[mikeselectrictuff]浮现在脑海中。如果你能成为这个部落中的一员，请在下面的评论中告诉我们你的理由。

早在 2016 年，我们就写过一个类似的用于 SMD 部件的[通用分线板，这是一个用于两针和三针软糖组件的单个分线板。如果你将其中一些板与[Travis]的分线板配对，这将是一个很好的组合，可以放在你的原型制作小工具箱中。下次你最喜欢的 PCB 商店打折时，考虑这个项目。](https://hackaday.com/2016/04/16/one-smt-breakout-to-rule-them-all/)