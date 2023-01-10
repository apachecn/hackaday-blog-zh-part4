# 为新的 Arduino 竞争对手腾出空间——使用原生 Brainf*ck！

> 原文：<https://hackaday.com/2021/01/12/make-room-for-a-new-arduino-competitor-with-native-brainfck/>

市场上有这么多更小、功能更强的微控制器板，现在可以相当肯定地说，经典的 Arduino 尺寸和外形已经过时。但这并不是说旧的竞争对手已经没有竞争力了，为了证明这一点，这里有一个新的平台，它采用了受人尊敬的基于 Atmel 的董事会设定的熟悉风格。[Eduardo corp EO]的 [Brainfuino 是 Arduino 的竞争对手，它运行每个人都喜欢的深奥编程语言 Brainf*ck](https://hackaday.io/project/176757-brainfuino) 。(保持 SFW，各位。)

如果您将它误认为 PCB 上的 Brainf*ck 仿真器，那么请准备好接受纠正，因为该板[在 Lattice MachXO2 FPGA](https://github.com/kuashio/bf) 上的 Brainf*ck 软核中本地运行该语言。这是真正的交易，只有真正的天才或受虐狂才敢在上面编码。

电路板本身的图形风格非常简洁，不仅仅是对原始 Arduino 的认可。该板上有 FPGA、256 kB ROM 和 138 kB RAM、提供 USB 串行端口和模拟输入的 STM32，以及在引脚上提供 Arduino 式 5 V 逻辑的电平转换器。我们可以看到，它将为任何有兴趣学习 Brainf*ck 的人提供数小时的乐趣，但除此之外，它还有可能成为 Arduino 形状的 FPGA 板。我们喜欢这个笑话，我们喜欢图形和工程设计，但在这背后隐藏着相当大的技术成就。

Brainf*ck 以前也成功过黑客日，尤其是这台令人瞠目结舌的中继计算机。