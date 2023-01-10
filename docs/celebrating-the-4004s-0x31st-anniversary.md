# 庆祝 4004 诞生 31 周年

> 原文：<https://hackaday.com/2020/11/16/celebrating-the-4004s-0x31st-anniversary/>

本周末是传奇的英特尔 4004 微处理器 49 周年纪念日，为了庆祝[Erturk Kocalar]在这个有趣的[retro shield 4004/Busicom 141-PF 计算器](http://www.8bitforce.com/projects/4004/)项目中结合了新老技术。我们之前已经报道过他的 [Arduino shield 项目](https://hackaday.com/2019/04/14/add-a-host-of-8-bit-processors-to-your-arduino/)，它可以让你将各种旧的微处理器连接到一个 Arduino 上，这样你就可以毫不费力地试验这些旧芯片。

[Erturk]决定使用 Arduino 来模拟 [Busicom 141-PF](http://www.vintagecalculators.com/html/busicom_141-pf_and_intel_4004.html) 的硬件，这是一款以给我们带来微处理器而闻名的计算器。除了计算器，Arduino 还必须模拟英特尔 4004 CPU 的支持芯片，包括 ROM、RAM 和移位寄存器。如果你想自己造一个，所有的设计文件都是开源的，或者你可以从他的 Tindie 商店得到一个组装好的盾牌。无论是哪种情况，你都必须提供你自己的 4004，令人惊讶的是，它仍然是可用的。(Tindie 和 Hackaday 共享同一个母公司，Supplyframe。我们和情报没有任何关系。)

我们非常感谢[Erturk]对计算器内部工作原理的详细解释。将仿真器连接到运行在 4004 上的原始 ROM 代码并不简单——例如，看看旋转鼓打印机的解释。我们喜欢细读带注释的 ROM 列表，也喜欢阅读 T2 为防止这些历史文件永远丢失所做努力的故事。如果你想更深入地研究，一定要看看[4004](https://hackaday.com/2018/01/29/inventing-the-microprocessor-the-intel-4004/)和它的[发明者费德里科·费金](https://hackaday.com/2018/06/19/federico-faggin-the-real-silicon-man/)的历史。