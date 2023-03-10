# ULX3S:一款开源点阵 ECP5 FPGA PCB

> 原文：<https://hackaday.com/2019/01/14/ulx3s-an-open-source-lattice-ecp5-fpga-pcb/>

萨格勒布创客空间 Radiona.org 的黑客们一直在努力设计用于 LATTICE ECP5 FPGAs 的开源开发板 ULX3S。该板可能有助于使 2019 年成为黑客 FPGA 年，在 2018 年没有完全实现后，黑客 FPGA 的出现再次被预测。即使快速浏览一下电路板和围绕它的开源开发也暗示着这次可能会有所不同。

[![](img/3bc7046abf56eea5b1190d8801f2db7b.png)](https://hackaday.com/wp-content/uploads/2019/01/ulx3s-bottom-view.png)

Bottom side of ULX3S PCB

ULX3S 主要是作为本科数字逻辑课程的教学工具而开发的。因此，它属于 FPGA 板的“厨房水槽”类别，包括一整套用于开发的外设和器件，而不是更简单的 FPGA 突破。该板包括 32 MB SDRAM、通过 ESP-32 的 WiFi(支持空中更新)、用于 SPI 有机发光二极管显示器的连接器、USB、HDMI、microSD 插槽、8 个 12 位 ADC 通道(1 MS/s)、实时时钟、56 个 GPIO 引脚、6 个按钮、11 个 LED 和用于 433 MHz FM/ASK 的板载天线。对于学生和任何开始 FPGA 开发的人来说，这似乎是一组很好的 I/o。

ULX3S 支持 Lattice ECP5 FPGA 系列的成员，范围从 12F(12k lut)到 85F(84k lut)。这么大的 FPGA 马力能做什么？看看 [ULX3S 链接报告](https://github.com/RadionaOrg/ulx3s-links)中的一长串例子。在那里，您可以找到从复古计算到复古游戏的代码，常见的 LED 和 HDMI 演示，甚至是运行在 mor1kx OpenRISC 内核上的 Linux。然而，回购中最有趣的环节可能是那些展示如何使用完全开源的工具链对 FPGA 进行编程的环节。专有工具链是阻止一些供应商的 FPGAs 在 OSHW 社区被广泛采用的最后一个环节，很高兴看到人们在逐步淘汰它们。

该板本身是完全开源的。在 [GitHub repo](https://github.com/emard/ulx3s) 中，你会发现在 MIT 风格的许可下发布的 PCB 的 KiCAD 5 设计文件。更令人印象深刻的是自述文件中的建议，它不仅欢迎独立生产主板，还就制造过程中如何与 PCBA 供应商打交道给出了一些可靠的建议。我们自己的建议是做正确的事情，如果你决定独立销售这款主板，即使许可证没有要求你这样做，也要给开发者提成。如果你想要一个，但不想自己制造，你可以使用 [ULX3S 页面](http://radiona.org/ulx3s/)底部的电子邮件或 gitter 链接联系开发者:他们目前正在进行小规模生产。

Radiona Org 的人制作了一些展示示例代码的视频。休息之后，看看板载 ESP-32 如何运行一个 web 服务器，该服务器可以将比特流加载到 FPGA 中(在这种情况下是为了一些复古游戏)。

 [https://www.youtube.com/embed/cgYtZW4zPSI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cgYtZW4zPSI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你是 FPGA 开发新手，不太确定从哪里开始，看看我们在 hackaday.io 上收集的一些 [FPGA 教程。一些 ULX3S 开发者也经常在我们自己的](https://hackaday.io/list/160076-fpga-tutorials) [FPGA 聊天室](https://hackaday.io/messages/room/272500)上闲逛，这是一个寻求关于 FPGA 所有事情的建议的好地方。

我们之前讨论过 FPGA 开发板，例如 [FleaFPGA Ohm，它也使用 ECP5](https://hackaday.com/2016/10/02/hackaday-prize-entry-fpgas-for-the-raspberry-pi-zero/) 。

感谢[Igor]的提示！