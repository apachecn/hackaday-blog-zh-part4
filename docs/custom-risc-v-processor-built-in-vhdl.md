# 用 VHDL 构建的定制 RISC-V 处理器

> 原文：<https://hackaday.com/2021/08/03/custom-risc-v-processor-built-in-vhdl/>

虽然 ARM 继续进军个人计算机市场，与英特尔和 AMD 等传统芯片制造商竞争，但它并不是一个完美的架构，确实有一些缺点。虽然这是迈向软件和硬件自由的一大步，但它并不是完全免费的，因为它需要一个许可证才能构建。有一个完全开源和免费的架构，被称为 RISC-V，它的设计和理念允许任何人构建和试验它，就像这个构建用 VHDL 实现了 RISC-V 处理器。

由于处理器是用 VHDL 语言构建的，这是一种允许设计和模拟集成电路的语言，因此可以下载处理器的代码，然后将其编程到几乎任何 FPGA 中。处理器本身称为 NEORV32，设计为片上系统，具有 GPIO 功能，当然还有完整的 RISC-V 处理器实现。该项目的创建者[Stephan]在第一次了解 RISC-V 时也很挣扎，所以他竭尽全力确保这个项目有完整的文档记录，易于设置，并且可以开箱即用。

当然，由于它是完全开源的，不需要像 ARM 平台那样麻烦的许可协议，所以它能够以任何需要的方式轻松修改或增强。所有的代码和文档都可以在项目的 [GitHub 页面](https://github.com/stnolting/neorv32)上找到。这是完全开源硬件(或软件)的真正好处，我们都可以支持它，即使目前对 [RISC-V 个人电脑](https://hackaday.com/2019/02/11/building-a-risc-v-desktop/)的选择仍然有限。

这与 [VexRISC](https://hackaday.com/2017/07/21/vexriscv-a-modular-risc-v-implementation-for-fpga/) 或 [PicoSOC](https://hackaday.com/2018/11/26/risc-v-cpu-gets-a-peripheral/) 相比如何？我们还不知道，但我们总是期待有选择。