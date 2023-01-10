# 将 Dreamcast 控制器与 Arduino 接口

> 原文：<https://hackaday.com/2021/03/19/interfacing-the-dreamcast-controller-with-just-an-arduino/>

Dreamcast 如今已经有点被人遗忘了，但在 20 世纪 90 年代末的辉煌时刻，人们可能会相信世嘉仍在战斗。不管怎样，它们的硬件仍然存在，被收藏家和爱好者们亲切地保存着。[Nicholas FitzRoy-Dale]就是这样一个爱好者，他着手将旧游戏机的控制器连接到 Arduino 上。

最初的工作包括让 Arduino(大概是一个基本的 16 Mhz Uno)读取控制器的按钮，并通过串行传输数据。Dreamcast 的枫树巴士速度很快，这带来了一些挑战，但它足够简单。[Nicholas]然后继续连接 VMU，Dreamcast 的奇特的控制器安装存储卡。在最初的尝试不稳定之后，他加倍努力。研究表明，VMU 可以改变它控制的汽车的速度，所以他更新了他的代码来适应。它充满了很棒的技巧，比如将 Dreamcast 的两个数据引脚连接到 Arduino 的四个输入引脚，通过不必转移输入数据来节省一些周期。

这项工作对于任何研究汇编级接口优化以及合理使用有限资源的人来说都是一个很好的读物。显然，很容易用更快、更贵的微控制器来解决这个问题，但是没有人会学到任何东西。多年来，我们推出了许多 Dreamcast hacks[Nicholas]在这里的工作[建立在[Dmitry]2017 年的工作基础上。](https://hackaday.com/2017/07/17/completely-owning-the-dreamcast-add-on-you-never-hadcompletely-owning-the-dreamcast-add-on-you-never-had/)我们迫不及待地想看到地下世嘉黑客场景的下一步是什么！