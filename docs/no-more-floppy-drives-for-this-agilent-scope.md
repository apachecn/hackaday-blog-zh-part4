# 安捷伦示波器不再需要软驱

> 原文：<https://hackaday.com/2020/05/10/no-more-floppy-drives-for-this-agilent-scope/>

当[kiwih]拿起一个 Agilent 54621A 示波器时，他觉得很有趣，因为它有一个软盘。曾经，使用磁盘将示波器数据传输到计算机是一项高科技。今天，没有那么多。然而，背面是一个串行端口。从那里读取数据肯定是可能的。是的，结果是找到端口的信息并使用 Python 与它进行交互。

通常，你会使用随附的 BenchLinkXL 软件从端口获取数据，但该软件太旧了，无法在 Windows 10 或 Wine 下运行。搜索没有在串行端口上找到太多东西，但是找到了一个类似安捷伦示波器的手册。该手册没有太大的帮助，因为它假设你是通过局域网或 USB 连接。然而，它确实提到了一个同样相似的旧型号，这是找到一本解释串行端口协议的手册的关键。

命令集看起来可疑地像[SCPI](https://en.wikipedia.org/wiki/Standard_Commands_for_Programmable_Instruments)——可编程仪器的标准命令——它是 GPIB 协议之上的一层。许多示波器都使用这种语言，所以这并不奇怪。这也意味着，如果你想与 SCPI 示波器交流，你可能会发现[代码很有用](https://github.com/kiwih/agilent-rs232)，即使你不使用串口或没有这种精确的安捷伦型号。

SCPI 有很多用途。例如，尝试[与你的作用域](https://hackaday.com/2016/03/29/you-speak-your-scope-obeys/)对话。廉价的 Rigol 和类似的望远镜通常有 SCPI，你可以使用[同样的技术](https://hackaday.com/2015/06/06/controlling-a-rigol-with-linux/)来控制和读取它们。