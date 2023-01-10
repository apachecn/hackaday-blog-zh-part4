# 电阻器分类器测量值

> 原文：<https://hackaday.com/2020/05/23/resistors-sorter-measures-values/>

我们都经历过。一大包电阻都混在一起了。也许你买得便宜。也许你整洁有序的抽屉洒了。当然，你可以痛苦地一个接一个地阅读颜色代码。或者使用计价器。但不管怎样，这都是一项乏味的工作。[Ishann]的解决方案是建立一个[自动分拣机，使用分压器](https://www.instructables.com/id/Resistor-Sorter-1/)直接测量价值，而不是像这些项目中常见的那样依赖机器视觉。这意味着可以对其进行修改，以实现精密电路的匹配(例如，挑选出所有标有 1K 且偏离一个标称值超过 0.5%的电阻)。

有一个漏斗，每次允许一个电阻进入测试区域进行测量。底部的板根据测量值旋转。在当前实施方案中，电阻要么向左，要么向右。将[做成一个带有隔间](https://hackaday.com/2016/12/30/sorting-resistors-with-3d-printing-and-a-pic/)的旋转托盘并不难，因为不同的阻抗值。看起来你必须一次一个电阻地给机器供电，考虑到松散的轴向元件是多么的混乱，自动化听起来像是一个诡计。尽管如此，这是一个有趣的项目，你可能有所有的零件。

一个 Arduino 驱动这个东西。液晶显示屏和显示器控制行动。如果你想练习用机器人处理材料，这是伺服系统和重力的一个很好的用途，它确实有实用价值。

我们已经看到了这方面的许多变化，包括[读取颜色代码](https://hackaday.com/2015/09/12/resistance-is-theres-an-augmented-reality-app-for-that/)的变化。如果你曾经想知道电阻器的[色码来自于](https://hackaday.com/2020/01/13/why-do-resistors-have-a-color-code/)，我们今年早些时候进行了一次回到过去的旅行来寻找答案。

 [https://www.youtube.com/embed/13Sx9HWPGfg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/13Sx9HWPGfg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

