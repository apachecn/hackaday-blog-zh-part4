# Glasgow 使用 FPGA 作为嵌入式系统的多功能工具

> 原文：<https://hackaday.com/2020/08/10/glasgow-uses-an-fpga-as-an-embedded-systems-multitool/>

每个构建嵌入式系统的人都希望有工具来帮助更快地构建和调试系统，所以我们经常会看到主板配备了各种工具，比如串口嗅探器。我们已经看过几个化身，最新的是格拉斯哥。该小型板使用 FPGA，并声称具有以下功能:

*   具有自动波特率确定功能的 UART
*   SPI 或 I2C
*   读写普通 EEPROMs 和闪存芯片
*   读写普通 EPROMs，包括数据救援功能
*   通过 SPI 对 AVR 芯片编程
*   播放 JTAG SVF 文件
*   调试 ARC 和一些 MIPS CPUs
*   程序 XC9500LX CPLDs
*   与多个无线电台和 CPU 通信
*   做声音合成
*   从软盘驱动器读取原始数据

revC 板是第一个相对实用的板，具有 16 个 I/O 引脚，工作频率高达 100 MHz，尽管文档暗示 6 MHz 可能是最容易实现的。软件是用 Python 和 [iCE40 FPGA 工具链](https://hackaday.com/2015/05/29/an-open-source-toolchain-for-ice40-fpgas/)编写的，我们过去已经讨论过很多次了。

这看起来已经是一个有用的工具，FPGAs 的可重构特性使其成为一个很好的扩展平台。文档讨论了调试主板的困难，因此基础软件提供了内置逻辑分析仪等支持。

我们已经看到开发板变成了工作台工具，比如[使用冰棍](https://hackaday.com/2016/12/13/compiling-a-22-analyzer/)作为[逻辑分析仪](https://hackaday.com/2016/12/13/compiling-a-22-analyzer/)。很高兴看到这样的专用工具围绕 FPGAs 的速度和多功能性而构建。