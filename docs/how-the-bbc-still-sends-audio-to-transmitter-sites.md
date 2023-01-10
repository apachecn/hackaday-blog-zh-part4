# BBC(静态)如何向发射台发送音频

> 原文：<https://hackaday.com/2022/09/13/how-the-bbc-still-sends-audio-to-transmitter-sites/>

表面上看，经营一家广播电台是一项简单的技术挑战。建造一个工作室，把它和发射器连接起来，你就可以开始了。但是，如果你的电台不是一个单一的反叛电台风格的山顶设施，而是一个由各种城市工作室提供信号的全国发射站链，会发生什么呢？这是英国广播公司国家英国调频发射机链面临的问题，自 20 世纪 80 年代以来，它一直由一系列 NICAM 数字数据流提供。我们在 2016 年提到过如何在没有任何听众注意到的情况下，用基于 FPGA 的现代实现替换老化的设备，现在多亏了[Matt Millman]，[我们有机会看到 20 世纪 80 年代的原始设备被拆除](https://www.mattmillman.com/nicam-ii-bbc-engineering-opens-the-archives-shows-us-some-vintage-kit/)。从 21 世纪 20 年代的角度来看，这项技术相对容易理解，但它仍然包含一些惊喜。

在每个演播室或发射机站点，都有一个 19 英寸的机架，其中包含一个这样的单元——一个带有编码器或解码器卡的卡框。这些都是由 BBC 的工程部门按照非常高的标准定制的，并使用了人们熟悉的 Z80 微处理器和一些飞利浦数字音频芯片等时期的部件，高端消费音频的追随者可能会认出这些芯片。正如您对任务关键型设备的预期，许多功能都是冗余的，通过比较它们的输出来发出故障警告。

令人惊讶的是 NICAM 编码器和解码器——这是专门为 BBC 定制的 LSI 芯片。这表明了国家广播公司可用的预算，鉴于这些单位在某些情况下已经工作了 35 年以上，我们猜测许可证支付者的钱花得值。

你可以阅读 2016 年的[原始切换，以及](https://hackaday.com/2016/01/23/35-million-people-didnt-when-zynq-took-over-their-radio/)[关于 NICAM](https://hackaday.com/2022/07/10/remembering-nicam-deep-dive-into-a-broadcasting-legacy/) 的更多信息。