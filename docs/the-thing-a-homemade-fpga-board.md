# “那个东西”:自制的 FPGA 板

> 原文：<https://hackaday.com/2019/10/17/the-thing-a-homemade-fpga-board/>

*这个东西*是一个[雄心勃勃的项目](https://hackaday.io/project/163683-the-thing-fpga-stm32)的不起眼的名字，该项目利用容易找到的元件来构建 FPGA 板。

该项目源于由[Just4Fun]提交给 2018 年 Hackaday 奖的早期构建,其中两个开发板——一个基于 STM32 的 Arduino 和一个 Altera MAX II CPLD 板——与 Arduino 相结合，用作 CPLD 的刺激发生器。这样，通过 USB 接口的 Arduino IDE 就可以用于对 CPLD 进行编程。

类似地，它使用 STM32 Arduino 作为 FPGA 的配套处理器，具有 512KB SRAM 和通用 I/O 用于 GPIOs，以及 PS/2 键盘用于运行 HDL SOCs。它还可以运行 Multicomp VHDL SOCs，这是一种模块化设计，用于运行[Grant Searle]制造的一些旧的 8 位 CPU。

FPGA (EP2C5T144C8N)使用 Quartus II IDE 通过 JTAG 或 AS 连接器配置 USB Blaster 加密狗。FPGA 侧控制一个 4 位 7 段 LED 显示器、4 个按钮、3 个 LED、一个清除所有内部 FFs(采样速率)的按钮、一个强制重启(重新加载配置)的按钮和一个强制所有引脚进入 Hi-Z 模式的开关。FPGA 侧还提供了板载 50MHz 振荡器和外部振荡器连接器。

在该板的 MP/M 系统功能的一次演示中，*部件*用于处理四个并发用户，一个串行端口连接器连接到 PC 和终端仿真器，另一个串行端口通过双通道 RS232 适配器板连接到 VT100 板上的终端仿真器。

Arduino 和 FPGA 都可以作为独立的电路板使用，但是如果可以将两个电路板结合在一起，为什么还要使用一个呢？

 [https://www.youtube.com/embed/j8qfqlEfJm8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j8qfqlEfJm8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)