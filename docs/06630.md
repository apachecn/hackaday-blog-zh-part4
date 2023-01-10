# 在 8087 数学协处理器芯片中寻找圆周率

> 原文：<https://hackaday.com/2020/05/20/looking-for-pi-in-the-8087-math-coprocessor-chip/>

即使有十个手指，数学也可能很难。微处理器的硅当量只有两个手指，在计算时会更加困难，经常需要多个机器周期才能算出像圆周率这样简单的东西。因此，40 年前，英特尔决定给其羽翼未丰的微处理器一个机会，推出 8087 浮点协处理器。

如果你曾经想知道 8087 内部发生了什么，请不要再想了。[【Ken Shirriff】已经解封了一个 8087](http://www.righto.com/2020/05/extracting-rom-constants-from-8087-math.html) 揭示了它的内部结构，原来和它的功能密切相关。在快速浏览了芯片的总体布局(包括找到微码引擎和 ROM)并快速查看了这项已有 40 年历史的技术的 NMOS 架构之后，[Ken]深入研究了协处理器的实质，以及它能够将某些浮点计算速度提高 100 倍的原因。复杂的芯片中有很大一部分是专用于只读存储器的，只读存储器除了存储计算算法所需的常数之外什么也不做。通过仔细检查 ROM 区域中 NMOS 晶体管的模式并进行一些有根据的猜测，他能够看到常数的二进制表示，例如圆周率和 2 的平方根。还有一系列广泛的反正切和对数 [2] 常数，用于[cord IC 算法](https://hackaday.com/2018/09/07/cordic-brings-math-to-fpga-designs/)，它将原本复杂的超越计算简化为一些快速简单的逐位移位和加法。

[肯]之前已经开发了很多芯片，在运算放大器中发现了[蝴蝶，在辛克莱科学计算器](https://hackaday.com/2018/06/27/ken-shirriff-found-butterflies-in-his-op-amp/)中发现了[逆向工程。但是看到硅中硬编码的常数确实让我们着迷。](https://hackaday.com/2013/08/30/ken-shirriff-completely-reverse-engineers-the-1974-sinclair-scientific-calculator/)