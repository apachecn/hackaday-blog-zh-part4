# 使用 555 定时器和逻辑综合实现 CPU

> 原文：<https://hackaday.com/2021/12/17/implementing-a-cpu-using-555-timers-and-logic-synthesis/>

在这里的页面上有很多评论，类似于“当你可以很容易地使用 555 定时器时，你为什么要使用微控制器！”是的，我们有时同意这种观点，但当 Hackaday.io 用户[Tim bs cke]看到一个偶然的评论，建议将它转变过来，用 555 个定时器构建一个微控制器时，这个挑战被彻底地抛出了。现在让我们澄清一下，这不是我们第一次遇到这个想法，十年前就有一个基于[试验板 555 的构建](https://hackaday.com/2011/08/05/building-a-computer-out-of-555-chips/)，但这是我们第一次看到它通过利用针对 PCB 的开源合成来实现！

第一个逻辑元件是一个简单的反相器，由 TRIGger 和 THReShold 引脚构成。

![](img/b752d4a30657e41e3e7fa45007ae117c.png)

LTSpice model of a NAND gate implemented with 555 and diodes

从此，只需在输入端添加几个二极管-电阻网络，就能实现 NAND2 门和 NOR2 门。通过在 LTSpice 中建模逻辑电路，找到器件值的最佳组合，开发速度有所加快。从这些简单的元素中，可以实现所有进一步的逻辑功能。接下来需要一个存储元件。幸运的是，555 有一个 RS 触发器作为其电路的一部分，由双比较器输入供电。所有需要做的就是将 THRS 输入偏置到 Vdd/2，然后通过传输晶体管馈入数据，嘿，很快！一个有用的，虽然很慢的门闩。

[Tim]之前创造了一个名为 [MCPU](https://github.com/cpldcpu/MCPU/blob/master/mcpu.pdf) 的极简 CPU，只有四条指令，旨在适应 32 宏单元 FPGA，因此能够在这个项目中重用该设计。有趣的部分是利用 [PCBFlow 工具链](https://github.com/cpldcpu/PCBFlow)【Tim】维护，它实现了一个带有自定义布局布线(PnR)后端的 Yosys 合成流。制作了一个 [liberty 文件](http://web.engr.uky.edu/~elias/lectures/LibertyFileIntroduction.pdf)，描述了【蒂姆】想要使用的电路(宏单元)，然后一个综合脚本使用 Yosys/GHDL 实现了流程，以阐述设计，将其映射到之前定义的技术中，并写出 PnR 工具可以使用的网表。有帮助的是，Yosys 还写出了设计的 PDF 以及 spice 网表。多好的工具！

为 PCBFlow 创建的 PnR 工具[Tim]是用 python 编写的，输出 Eagle 可以使用的 XML 格式。它的工作是通过查找适当的物理电路(包括所有无源器件)，将宏单元放入 PCB，添加互连，然后使用模拟退火优化布局，优化最小走线长度，从而放置宏单元(特意制成方形)。我们认为结果看起来非常漂亮，这种方法可以很容易地在未来的其他项目中重用。

感谢[YGDES]发送此邮件！