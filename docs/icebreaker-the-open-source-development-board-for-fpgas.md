# 破冰者，FPGAs 的开源开发板

> 原文：<https://hackaday.com/2018/12/13/icebreaker-the-open-source-development-board-for-fpgas/>

Hackaday 超级会议结束了，这很遗憾，但我们会议的一个伟大之处是人们每年都设法跋涉到帕萨迪纳向我们展示他们正在研究的所有很酷的东西。其中一个人是 1 Bit Squared 的创始人(Piotr Esden-Tempski)，他带来了一些很快将在一些众筹平台上推出的好东西。[其中最酷的是破冰者](https://www.crowdsupply.com/1bitsquared/icebreaker-fpga)，这是一个 FPGA 开发套件，通过开源工具链可以轻松学习 FPGA。

破冰船的硬件包括 iCE40UP5K fpga，具有 5280 个逻辑单元、120 kbit 双端口 RAM、1 Mbit 单端口 RAM 以及一个 PLL、两个 SPI 和两个 I2C。因为最有趣的 FPGA 应用包括通过引脚非常非常快速地发送位，还有 16 兆 SPI 闪存，允许您将视频流传输到 LED 矩阵。这里也有足够的逻辑单元来合成一个 CPU，并且破冰船已经可以处理 [PicoRV32](https://github.com/cliffordwolf/picorv32/) 和一些 [RISC-V](https://riscv.org/) 内核。可扩展性是通过 PMOD 连接器，是的，还有一个 HDMI 输出为您的老式计算项目。

如果你想进入 FPGA 开发领域，这是最好的时机。Joe Fitz 来自 2018 Hackaday Superconference 的 WTFpga workshop 已经被[转换成了这个破冰板](https://github.com/esden/WTFpga)，是的，七段显示和 DIP 开关可用。在这个工具链和开源的 iCE 工具链之间，你已经有了一个完整的开发系统，可以随时使用，玩起来很有趣，而且功能非常强大。