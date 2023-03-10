# 本周失败:当涂有环氧树脂的芯片导电时

> 原文：<https://hackaday.com/2018/11/18/fail-of-the-week-when-the-epoxy-coated-chip-is-conductive/>

每隔一段时间，你会发现一些奇怪的事情，让你头晕目眩。大多数时候，你会把它归因于一个糟糕的焊点，一些糟糕的代码，或者仅仅是你自己的失误。这次不一样了。这是一个奇怪的故事，完全是因为一个不应该在那里的别针。[这是一个具有零引脚](https://mcuoneclipse.com/2015/09/29/learning-from-failure-qfn-package-corner-problem/)的集成电路封装。

故事从[Erich]为 Freescale Kinetis K20 FPGA 构建几个开发板开始。这是一个支持 USB 的微控制器，从各方面来看，这是一项值得做的工作。到目前为止，一切顺利。原型板的问题很快就显现出来了。在某些板上，外部 32 kHz 振荡器没有启动。重新焊接振荡器或微控制器*有时*解决了问题，但并不总是如此。这很麻烦，因为这意味着问题不在于代码，也不在于 PCB。这将需要一个深潜和一个良好的检查显微镜。

[![](img/af7701b0939a40cdf7be4701859b8347.png)](https://hackaday.com/wp-content/uploads/2018/11/ground-pad-on-the-outside.png) 【埃里希】的一个朋友【克里斯蒂安 B】不知怎么发现了问题。制造飞思卡尔 K40 时，芯片被小心地放置在芯片载体中，并涂上环氧树脂，将其放入小型 QFN 封装中。问题是，这个芯片的一角伸出了一个额外的连接。这只是芯片载体的一个产物，但如果你让裸露的金属接地，最终会出问题。

[Erich]最有可能的猜测是，这种额外的连接来自制造和封装过程，本应用中的裸露金属焊盘与相邻焊盘相连。现在，如果[Erich]的设计有一个失败之处，那就是走线以 90 度从相邻焊盘的引脚出来；这不是最佳实践，但大多数情况下您可以侥幸逃脱。不过，这一次，有人受伤了。

我们不知道[克里斯蒂安]是如何发现这个问题的。当你看到一个微小的 QFN 封装时，你不会期望有一个额外的引脚连接到地，可以很容易地用一点焊膏桥接。发现这个问题要么需要很大的运气，要么需要很高的技巧，但这是一个很好的例子，说明了你必须要注意的奇怪的事情。