# 基于继电器的伪随机数发生器

> 原文：<https://hackaday.com/2020/12/09/a-relay-based-pseudorandom-number-generator/>

有很多种方法可以构建一个随机数生成器，同样也有很多方法可以生成看起来是随机的数字，但从纯数学意义上来说通常不是。[Daniel Valuch]建造了一个圣诞装饰品，它做了后者，在一个吸引人的闪光装饰品上显示结果。

该构建依赖于 16 位[线性反馈移位寄存器](https://en.wikipedia.org/wiki/Linear-feedback_shift_register#Fibonacci_LFSRs)，或 LFSR。LFSR 产生一个数字流，每个数字取决于寄存器的先前状态。因此，生成的数字是伪随机的，而不是真正随机的，并且取决于系统的初始种子值。[Daniel]使用继电器和发光二极管构建了移位寄存器，继电器在寄存器运行时产生可爱的咔嗒声，发光二极管根据寄存器中的值发光。

结果是一个可爱的圣诞装饰品，以确定的方式闪烁，由于 PCB 的裸露铜和使用的复古 LED 颜色，具有很好的老派外观。该项目也是学习移位寄存器和基本继电器逻辑的一个很好的途径，尽管后者现在很少用于严肃的目的。我们以前也讨论过这个话题。休息后的视频。

 [https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLIZ-1iHyG9xV1FDpP2osFapAvcU9Ouz1K](https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLIZ-1iHyG9xV1FDpP2osFapAvcU9Ouz1K)

