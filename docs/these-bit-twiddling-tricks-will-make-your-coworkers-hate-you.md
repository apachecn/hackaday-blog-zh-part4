# 这些小把戏会让你的同事讨厌你

> 原文：<https://hackaday.com/2020/01/16/these-bit-twiddling-tricks-will-make-your-coworkers-hate-you/>

在嵌入式领域，摆弄几个比特是正常的行为。固件在堆栈中的位置很低，以至于作者可能会关心所使用的位数和字节数，或者需要直接使用寄存器来让机器跳舞。通常这些操作仅限于典型的移位和掩蔽，但有时问题需要更奇特的解决方案。如果你需要深入这些黑暗的深处，你总是会遇到由肖恩·埃隆·安德森收集的经典的[小窍门](https://graphics.stanford.edu/~seander/bithacks.html)。这里有龙。

![](img/172c26b3df19e1a1845f244a89125efd.png)

Discussions of bit math are great opportunities to revisit [Wikipedia’s superb illustrations](https://en.wikipedia.org/wiki/Bitwise_operation)

Bit Twiddling Hacks 是完全一样的描述；这一页充满了如何以方便或有效的方式执行所有形式的位数学的片段和建议。让我们惊讶的是，在阅读页面顶部的免责声明时，[Sean]发现有如此多的人使用过该页面的内容，以至于它实际上都经过了彻底的测试。考虑到一些片段是多么深奥，我们很想知道最黑暗的角落是如何被利用的。

该页面包含了各种各样的巧妙技巧。像[统计设定位](https://graphics.stanford.edu/~seander/bithacks.html#CountBitsSetNaive)这样的采访内容提前出现。还有更深奥的内容，比如[将两个 u16 中的位交织](https://graphics.stanford.edu/~seander/bithacks.html#InterleaveTableLookup)成一个 u32 的技巧，或者[通过转换浮点数舍入到 2 的下一次幂](https://graphics.stanford.edu/~seander/bithacks.html#RoundUpPowerOf2Float)。这位作者只在一种情况下被迫求助于 Bit Twiddling Hacks:对一个不幸设计的具有不寻常长度寄存器的传感器的输出进行[符号扩展](https://graphics.stanford.edu/~seander/bithacks.html#FixedSignExtend)。

下次您需要使用 bitmatch 执行操作时，请查看 Bit Twiddling Hacks。你在生产中需要过吗？你是怎么用的？我们很想在评论中听到它。