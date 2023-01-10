# 一个负担得起的可编程序控制器

> 原文：<https://hackaday.com/2022/12/08/an-affordable-and-programmable-plc/>

我们都习惯了通用微控制器板，如 Arduino 或其许多模仿者，但也许我们没有看到太多的工业表亲。可编程逻辑控制器(PLC)是一种设计用于自动化工业机械的计算机，带有受保护的接口，通常还有特定的 PLC 编程环境。因此[【Galopago】与一个廉价的中国 PLC 克隆](https://galopago.github.io/english/repurposing-plc-clone-arduino/)的工作特别有趣，提供了一条在 Arduino IDE 生态系统中使用它的前进路线。

打开它，处理器被识别为 STM32F103，并识别出将其置于 bootloader 模式所需的连接。然后可以从 Arduino IDE 中对它进行编程，尽管它的引导装载程序不能更改。然后，为了完成这个过程，有必要通过老式的硬件逆向工程来识别各种不同的输入和输出。

这种 PLC 可能不像某些价格昂贵的产品那样稳定可靠，但它仍然是访问微控制器板的一种经济有效的方式，微控制器板上已经安装了控制机器通常所需的大部分接口电路。我们期望在接下来的几个月里我们会看到它出现在这些页面上，也许[甚至会有另一个比较在空中](https://hackaday.com/2017/07/17/plc-vs-arduino-show-down/)。