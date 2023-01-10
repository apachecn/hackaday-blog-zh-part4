# 需要 JTAG 适配器吗？用你的对讲机。

> 原文：<https://hackaday.com/2022/04/11/need-a-jtag-adapter-use-your-pico/>

JTAG 是一个强大的接口，用于各种设备的低级调试和自省，包括 CPU、FPGAs、MCU 和许多复杂的专用芯片，如 RF 前端。JTAG 适配器可能相当晦涩难懂，或者价格不菲，这就是为什么我们很高兴地看到来自[ADIUVO] [的[Adam Taylor]制作了一个关于使用 Pi Pico 板作为 JTAG 适配器的教程](https://www.adiuvoengineering.com/post/microzed-chronicles-jtag-using-a-raspberry-pi-pico)。这依赖于[一个由【Dhiru Kholia】开发的名为 XVC-皮科](https://github.com/kholia/xvc-pico/)的项目，除了 Pi 皮科板本身之外不需要任何东西——XVC-皮科提供了一个实现 XVC (Xilinx 虚拟电缆)规范的 RP2040 固件和一个连接到皮科板和 Vivado 等工具接口的守护程序。

本文的第一部分致力于使用 Linux VM 编译 Pico 固件。然而，GitHub repo 的[中有一个预建的`.uf2`二进制文件，所以你不必这么做。然后，他在连接 Pico 的 PC 上编译并运行一个守护程序，通过 Vivado 连接到该守护程序，并使用 Xilinx XC7Z020 在 MYIR Z-turn 板上成功单步调试代码。值得记住的是，如果您的 FPGA(或任何其他目标)的 JTAG 逻辑电平是基于 1.8V 或 2.5V，您将需要在它和 Pi Pico 之间有一个电平转换器，Pi Pico 是一个固定在 3.3V 范围内的板。](https://github.com/kholia/xvc-pico/tree/master/firmware)

你就是无法击败 3 美元的价格和安装的简易性。Pi Pico 越来越成为一个硬件多功能工具。就在一个月前，我们报道了 Pico 如何作为逻辑分析仪工作。其中很大一部分，我们要感谢 PIO 外围设备——一个状态机组件，它甚至可以让你“bit bang”[像 DVI](https://hackaday.com/2021/02/12/bitbanged-dvi-on-a-raspberry-pi-rp2040-microcontroller/#comments) 这样的高速接口。如果你对 PIO 如何运作感兴趣，[这里有一些很好的文章](https://hackaday.com/2021/01/29/a-look-at-the-interesting-rp2040-peripheral-those-pios/)。如果没有 Pi Pico，你也可以用这个主板的姐姐来和 JTAG 接口。