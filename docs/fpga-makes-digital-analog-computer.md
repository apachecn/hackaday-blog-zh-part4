# FPGA 制造数字模拟计算机

> 原文：<https://hackaday.com/2019/02/14/fpga-makes-digital-analog-computer/>

当您想到模拟计算时，您可能通常不会想到 FPGAs。当然，一些 FPGAs 会有专门的模拟模块，但通常都是数字器件。[Bruce Land]——Hackaday 熟知的一个名字——有一篇关于使用 FPGA 构建一个[数字差分分析仪](https://people.ece.cornell.edu/land/courses/ece5760/DDA/index.htm)的帖子，它本质上是在 FPGA 的数字结构上模拟的模拟计算机。

传统的模拟计算机使用运算放大器进行数学积分，而 FPGA [Land]使用数字加法器来模拟微分方程系统，该系统可以是非线性的。

当然，本质上它仍然是一个数字设备，用 18 位数字格式表示数量。虽然理论上能够实现无限分辨率，但实际模拟系统会受到噪底、元件变化和测量不确定性的限制，因此实际上 18 位足以满足大多数用途。然而，对于需要更高精度的应用，[Land]还扩展到 27 位。当然，ADI 公司与 FPGAs 一样，天生就是并行的，所以这部分匹配得很好。

示例代码在 Verilog 中，甚至有一个 CPU 与(模拟的)模拟计算机合作的例子。曾经，人们不清楚模拟计算机是否会接管世界。他们甚至制造了便携式的——如果你认为 28 磅是便携式的话。我们最近看到了一些关于[模拟计算机](https://hackaday.com/2019/01/29/continuous-computing-the-analog-way/)的帖子。也许他们会卷土重来。