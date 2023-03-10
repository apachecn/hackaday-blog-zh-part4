# 当你的逻辑分析仪不能区分好的和坏的信号

> 原文：<https://hackaday.com/2022/07/09/when-your-logic-analyzer-cant-tell-good-and-bad-signals-apart/>

[Avian]获得了一款 Miniware la 104——一款内置协议解码器的小型电池供电逻辑分析仪。当你需要快速了解某个信号的真实情况时，这种分析仪是很方便的工具，而且它们足够便宜，可以牺牲掉有风险的维修。可悲的是，[他偶然发现了一个特殊的问题](https://www.tablix.org/~avian/blog/archives/2022/03/waveform_display_bug_in_the_la104/)——分析仪会不时显示信号故障，即使是在非常低的比特率下。更令人惊讶的是，当输出并在笔记本电脑上查看时，信号轨迹中没有出现故障。

[![A Pulseview window showing that the problem is not present in the exported captures](img/55a131dc2dce8fe836330c3ebcd51e8a.png)](https://hackaday.com/wp-content/uploads/2022/07/hadimg_la104_issue_pic2.png) 他深究问题，[正如【禽】一样。](https://hackaday.com/2022/04/10/this-3-5mm-cable-distorts-signals-hides-audio-filtering-circuit/)浏览问题重重的捕获文件帮助他认识到，当信号边沿之一相对于其他信号边沿延迟几微秒时，故障就会发生——这在数字逻辑中是经常发生的。这似乎源于由 FPGA 驱动的分析器的“捕获样本并发送它们”部分所使用的压缩。这个错误只与分析仪屏幕上显示的信号有关，结果表明，虽然分析仪的大部分界面是由 STM32 CPU 绘制的，但轨迹绘制部分是由 FPGA 使用单独的 LCD 接口来完成的。

Miniware 似乎没有做足够的测试，并且在使用 LA104 时不可能区分好信号和坏信号，而 la 104 可以说是逻辑分析仪的主要功能。在最好的迷你软件传统中，有时甚至会敌视开源固件，FPGA bistream 源代码是专有的。因此，这个 bug 不是我们自己可以轻易修复的，除非 Miniware 升级并发布一个 gateware 更新。在那之前，如果你买了一个 LA104，你不能依赖它在屏幕上显示的信号。

当谈到迷你器皿问题时，我们最近报道了[一个迷你器皿镊子修理，](https://hackaday.com/2022/05/23/hackaday-prize-2022-glue-hindered-smart-tweezer-repair-involves-a-rebuild/)需要重新设计最初用大量胶水粘在一起的外壳。有时，感觉就像[充满胶水的不可修复的小玩意和有缺陷的专有固件之间有一些共同点](https://hackaday.com/2021/08/11/should-you-be-able-to-repair-it-we-think-so/)。如果这个 bug 毁了你的 LA104，嘿，至少你可以把它刷新到[作为电子接口多功能工具。](https://hackaday.com/2020/10/01/teaching-a-pocket-logic-analyzer-many-new-tricks/)