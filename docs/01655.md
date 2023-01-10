# QtCreator 学习 Verilog 时的 FPGAs 开源 IDE

> 原文：<https://hackaday.com/2018/12/29/open-source-ide-for-fpgas-as-qtcreator-learns-verilog/>

经典战役:PC 对 Mac，Emacs 对 Vi，美味对不饱，当然还有我们围绕 Hackaday watercooler 争论的一个问题:命令行还是 IDE？对于使用优秀的旧命令行工具，有一些东西要说，即使您喜欢将您最喜欢的编辑器配置为几乎是一个 IDE，至少它是一个您熟悉的编辑器，并且可以在几种不同的用途上使用。

大多数商业 FPGA 工具都带有一个重量级的 IDE。Lattice 的开源工具(IceStorm)通常由命令行或 makefile 驱动。直到现在。【Roch us-Keller】[发布 VerilogCreator，这是 QtCreator](https://github.com/rochus-keller/VerilogCreator) 的一个插件。

我们印象深刻，因为就 ide 而言，QtCreator 既有用又轻量，这两样东西对于许多类似的工具来说是不可同日而语的。[FPGAwars]已经有了一个基于 Atom 的 IDE([apio-IDE](https://github.com/FPGAwars/apio-ide))，尽管它已经有将近一年没有更新了。当然，IceStudio 看到了更多的更新，但与其说它是一个 IDE，不如说它是一个基于 GUI 的代码生成器。

[Rochus-Keller]说还有更多。然而，即使在这个早期阶段，IDE 也提供语法着色、工具提示、内联消息，并且可以分析源代码，允许您如预期的那样交叉引用符号。有供伊卡洛斯做模拟的配置，或者你可以使用 Verilator 或 Yosys——ice storm 背后的合成器。它似乎还可以与基于 Tcl 的工作流交互，就像大多数 FPGA 供应商 ide 所使用的工作流一样。

待办事项清单上还有很多，所以我们很期待看到事情的进展。QtCreator 不难学，也不像 Eclipse 这样的大型 ide 那样臃肿。如果你想快速了解 QtCreator，[我们已经介绍过了](https://hackaday.com/2016/07/08/join-the-gui-generation-qtcreator/)。如果你想画框而不是直接写 Verilog，可以试试 [IceStudio](https://hackaday.com/2016/02/23/icestudio-an-open-source-graphical-fgpa-tool/) 。