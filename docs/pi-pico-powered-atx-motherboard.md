# 皮皮科供电的 ATX 主板

> 原文：<https://hackaday.com/2021/06/22/pi-pico-powered-atx-motherboard/>

几年来，嵌入式开发人员和 Rust 上瘾者[Jonathan Pallant]又名[theJPster]一直在研究一台简单的计算机，他称之为 Neotron。这个想法是[制造一台不仅易于使用而且易于理解的计算机。他把它描述为一个用于小型 ARM 微控制器的类似 CP/M 或 DOS 的操作系统。他最近的项目由 Raspberry Pi RP2040 Pico 驱动，并以 microATX 主板的格式构建。这款主板为基于 Pico 的设计提供了许多功能，包括 12 位彩色 VGA 和 7 个扩展槽。参见](https://hackaday.io/project/180407-neotron-pico)[的 GitHub 库](https://github.com/Neotron-Compute/Neotron-Pico)获取完整的规范列表，以及构建自己的项目所需的所有文件——毕竟这是一个开源项目。

除了 Neotron Pico 本身，在这个记录丰富的项目中，一些宝石引起了我们的注意。Pico 上的 I/O 引脚快用完了，没有足够的剩余引脚用于所有外设的芯片选择。查看他如何使用 MCP23S17 SPI 总线 I/O 扩展器和三态缓冲器来解决问题。

在一个更元的层面上，我们对他使用 GitHub 动作很感兴趣。按照存储库的标准概念，它们不应该包含构建的结果，无论是可执行的二进制文件还是 Gerber 文件。构建产品的分发通常是在 GitHub 之外处理的，使用类似 GitHub 的大文件存储服务，或者完全忽略约定，将它们放入 repo 中。[theJPster]使用另一种方法，例如，使用 GitHub 动作来生成 PCB 制造所需的文件。

Neotron Pico 是运行 Neotron OS 的一系列主板中的最新产品。以前的主板包括:

*   Neotron 9x —微芯片 SAM9X
*   Neotron 1000 — STM32H7 +点阵 Semi iCE40 FPGA
*   Neotron 600 —青少年 4.1
*   neotron 340 ST—ST 32f 746g-发现

The [HackadayPrize2021](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)