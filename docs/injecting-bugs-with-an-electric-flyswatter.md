# 用电蚊拍注射虫子

> 原文：<https://hackaday.com/2021/03/15/injecting-bugs-with-an-electric-flyswatter/>

硬件故障注入使用数字电路的电气操作来有意引入错误，这可用于导致处理器以不可预测的方式运行。这种无意的行为可用于测试可靠性，也可用于更邪恶的目的，如访问本应不可访问的代码和数据。有几种方法可以实现这一点，电磁故障注入使用局部电磁脉冲来翻转处理器内部的位。该脉冲在处理器的电路中感应出一个电压，导致比特翻转，并经常导致无意的行为。做到这一点的硬件非常专业，但[Pedro Javier]设法将一个 4 美元的电苍蝇拍黑进了一个电磁故障注入工具。(页面可能死了，试试[互联网存档版](https://web.archive.org/web/20210312133612/https://pedrojavier.com/devblog/dirtcheapemfaultinjection/)。)

[Pedro]通过把一个电苍蝇拍变成一个火花隙触发的电磁脉冲发生器来实现这个。他把苍蝇拍的商业端拿掉，换上一个手绕电感器，串联一个小火花隙。按下改良苍蝇拍上的电源按钮，对输出电容器充电，直到产生的电压足以电离火花隙中的空气，此时电容器通过电感器放电。火花间隙的大小决定了积累的电荷——间隙越大，电荷越多，产生的脉冲越大，在芯片中感应出的电压就越大。

[Pedro]演示了如何使用它来产生算术错误，甚至诱导 Arduino 转储其内存。其他人[使用电磁故障注入来破坏 SRAM](https://circuitcellar.com/research-design-hub/electromagnetic-fault-injection/) ，而[故意干扰电源引脚](https://hackaday.com/2020/07/04/the-cheap-way-to-glitch-an-stm8-microcontroller/)也可以用来访问其他受保护的数据。