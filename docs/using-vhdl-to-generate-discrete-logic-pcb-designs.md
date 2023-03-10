# 使用 VHDL 生成离散逻辑 PCB 设计

> 原文：<https://hackaday.com/2021/11/13/using-vhdl-to-generate-discrete-logic-pcb-designs/>

VHDL 和 Verilog 是硬件描述语言，用于描述和定义逻辑电路。它们通常用于设计 ASICs 和编程 FPGAs，本质上是使用软件来定义硬件。然而，[Tim]做了一些非常有创意的事情，他创造了一些工具来利用 VHDL 和 Verilog[并为分立逻辑设计出 PCB。](https://hackaday.io/project/180839-vhdlverilog-to-discrete-logic-flow)

是的，你没看错。基本思想是采用 VHDL 源代码，然后利用电阻-晶体管逻辑制作实现所需逻辑的 PCB 布局。从那里，PCB 设计文件可以被运送到制造商那里进行取放组装，其成本只是定制 ASIC 生产成本的一小部分。

弊端显而易见；需要大量独立的分立器件，尺寸代价非常大，功耗几乎肯定比在 ASIC 甚至 FPGA 上做同样的逻辑高出几个数量级。哦，一切都慢多了。

然而，作为一项学术练习或者仅仅是为了娱乐，这是一项了不起的工作。人们可以定义一个复杂的逻辑电路，并让 PCB 实现由自动化工具产生的逻辑，这一想法令人惊叹，我们绝对希望看到更多这种类型的事情。

我们已经看到了将 VHDL 综合到 74 系列逻辑设计中的类似工作。如果你一直在开发你自己的奇特的数字逻辑赋，一定要给我们写信！

【感谢 Yann Guidon 的提示！]