# Symbiflow 开源 FPGA 工具链

> 原文：<https://hackaday.com/2019/11/01/symbiflow-open-source-fpga-toolchain/>

任何享受过 FPGAs 编程乐趣的人都知道，这是一个专有工具的世界，几乎需要对特定平台做出婚姻级别的承诺才能有效。Symbiflow 希望通过成为 FPGA 的 [GCC 来解决这个问题。](https://symbiflow.github.io/)

Symbiflow 将提供一个更加通用的界面，而不是围绕特定芯片或架构构建的工具。用户可以用 Verilog 编程；架构定义定义了如何为正确的芯片编译代码。他们目前的目标是广受欢迎的 Xilinx 7 系列、非常实惠的 lattice ice 40 系列以及 Lattice 的 ECP5 FPGAs。

如果你今年去 Hackaday Supercon，【Timothy Ansell】将[做一个关于 Symbiflow 如何让这个过程变得更加平易近人和更少专利的演讲](https://hackaday.com/2019/10/04/more-supercon-talks-taking-the-hardware-world-by-storm/)。总的来说，我们对通用接口感到非常兴奋，特别是当 FPGAs 的价格持续下降到微控制器领域，同时功能也在增加。

(说到 Supercon，也许这是一个剧透，如果没有 Symbiflow、Project Trellis、Yosys 和 NextPNR，徽章就不可能出现。)