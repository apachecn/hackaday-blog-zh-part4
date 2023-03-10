# 实现梦想:一款非常便宜的计算器手表的新 PCB

> 原文：<https://hackaday.com/2021/08/01/living-the-dream-new-pcb-for-a-dirt-cheap-calculator-watch/>

这个黑客让我们乐坏了。我们喜欢购买一些非常便宜的技术，并用它做一些令人惊讶的事情，这是一个教科书般的例子。[davedarko]在阿里快递上发现了最可爱的小计算器手表，并正在为它制作新的 PCB。计划是使用 ARM 处理器和 Arduino，并添加一些额外的功能，如 24 小时模式和粉红色(或潜在的 RGB)背光。新的大脑将是一个 ATSAML22G18A，它有一个板载 LCD 控制器和一个 I/O 引脚，无需重复按钮。

[davedarko]的主要目标之一是保持液晶显示器，并找出如何与它交谈。第一项工作是通过找出黑色环氧树脂下的秘密，对手表的 LCD 控制器进行逆向工程。这是一次大开眼界的经历，因为[davedarko]以前从未直接接触过液晶显示器。一个奇怪的读数使他打开了示波器。[长话短说](https://hackaday.io/project/180832-new-pcb-for-calculator-watch/log/195469-reverse-engineering-the-lcd-controller)，【davedarko】发现它使用 1/2 的偏置来产生复用段和保持信号交替所需的波形。这绝对值得一看！

我们喜欢这里的钟表，也见过各种各样的黑客，尤其是卡西欧手表。想要黑暗模式？[搞定](https://hackaday.com/2021/01/22/casio-f-91w-going-dark/)。启用隐藏倒计时定时器？[我们也有](https://hackaday.com/2021/04/30/modding-a-casio-w800-h-with-a-countdown-timer/)。你有没有想过[F91W 到底有多防水](https://hackaday.com/2021/06/18/just-how-water-resistant-is-the-casio-f91w/)？