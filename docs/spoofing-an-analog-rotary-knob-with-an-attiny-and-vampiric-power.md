# 伪装成一个有着吸血鬼力量的模拟旋钮

> 原文：<https://hackaday.com/2020/07/14/spoofing-an-analog-rotary-knob-with-an-attiny-and-vampiric-power/>

[Mitxela]修理一台 Roland JV-1080(一台架装式 90 年代合成器)听起来很简单:更换前面板上一个损坏的旋转编码器。[事实证明这一点也不简单](https://mitxela.com/projects/jv1080_encoder_repair)，因为这个零件根本不是今天的标准旋转编码器。JV-1080 使用某种旋转脉冲开关，它有三个输出(一个用于每个方向，一个用于像按钮一样推动旋钮。)向一个方向转动旋钮，每个棘爪的一条输出线会短暂地对地短路。反过来，另一条输出线上也会发生同样的情况。这是需要更换的零件。

[![](img/da9269ad5387b2fdd91c6c94327a91fe.png)](https://hackaday.com/wp-content/uploads/2020/07/jv1080_6.jpg)

The finished unit uses a modern rotary encoder and microcontroller in place of the original part, and implements a few tricks to power it.

[Mitxela]没有追踪损坏部件的来源，而是选择用现代旋转编码器结合 ATtiny85 微控制器来替换它，使它的行为像 JV-1080 理解和期望的那样。然而，还有另外一个问题。最初的旋转脉冲开关是一个完全无源的装置，位于一根四芯电缆的末端，没有电源。ATtiny85 怎么能不通过电线连接到某处的 DC 电源来供电呢？成功是有的，但确实需要一些技巧。

对于电源，结果是信号线被微弱地上拉至+5 V，并且[Mitxela]使用*和*作为微控制器的电源。尽管如此，这本身还不够，因为 ATtiny85 很容易消耗比弱上拉电源更多的电流。我们真的建议阅读[Mitxela]的文章中的所有细节，但简短的版本是 ATtiny85 做两件事。

首先，它通过大部分时间处于睡眠模式(几乎不消耗任何功率)来最大限度地降低功耗，并使用中断来唤醒足够长的时间来处理旋钮活动。第二，弱上拉的涓涓细流不会直接供给态度。它通过一个二极管给一个 100 uF 的电容器充电，这就是为什么微控制器在短暂的活动期间不会掉电。更妙的是，在浏览 ATtiny 的数据手册后，[Mitxela]发现可以使用内置 ESD 保护二极管来实现这一目的，而不是增加一个单独的元件。

这是一个巧妙的技巧，有助于实现非常紧凑的封装。[访问该项目的 GitHub 库](https://github.com/mitxela/jv1080-encoder)深入了解细节。最终，4 线连接器末端的单个组件就像原始无源元件一样工作，不需要额外的导线或硬件修改。

打开旧的硬件时，永远不知道里面会发现什么。但至少[Mitxela]在这个合成器上的维修任务没有以他服用迷幻药而告终。