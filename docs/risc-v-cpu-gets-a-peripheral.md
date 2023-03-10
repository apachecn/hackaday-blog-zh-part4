# RISC-V CPU 得到一个外设

> 原文：<https://hackaday.com/2018/11/26/risc-v-cpu-gets-a-peripheral/>

人们使用 FPGA 的方式之一是让 FPGA 结构的一部分容纳一个 CPU。这是有道理的，因为 CPU 擅长一些 FPGA 难以完成的工作，反之亦然。现在 RISC-V 体系结构已经可用，它可以用作基于 FPGA 的 CPU。[Clifford Wolf]创造了 pico SOC——一种 RISC-V CPU，可用作 SOC 或片上系统，带有 Lattice 8K 评估板。[Mattvenn]将其移植到 TinyFPGA 板上，该板也包含一个 Lattice FPGA，并向[展示了它与 WS2812 智能 LED 外设](https://github.com/mattvenn/TinyFPGA-BX/tree/master/examples/picosoc)的接口示例。你可以在下面看到一个关于这个项目的视频。

真正符合 RISC-V 的开源本质的是，该项目使用了我们之前多次讨论过的开源 Icestorm 工具链。[Matt]考虑周到地提供了预编译的固件，因此您不必为 RISC-V 安装 gcc，除非您想编写自己的软件。当然，你会的。

RISC-V 不是第一个可用于 FPGAs 的 SOC，尽管一些常用的 SOC 具有模糊的谱系，因为它们模拟了其他一些非开放的 CPU。视频的第一部分介绍了如何开始使用 RISC-V。然后[Matt]解释了他如何在设计中加入对智能 led 的支持。

附加部分是用 Verilog 写的，所以如果你不读这种语言，你可能想在着手这个项目之前复习一下。这个设计一经证实，他就将 LED 驱动器与 CPU 集成在一起。

虽然 SOC 硬件和软件设计并不是一个新的想法，但令人惊讶的是，现在您可以使用 gcc、icestorm 和开源 CPU 内核等开放工具来完成它。如果你想开始做一些不那么令人畏惧的事情，你可以随时查看我们的 [FPGA 训练营](https://hackaday.com/2018/08/06/learn-fpga-fast-with-hackadays-fpga-boot-camp/)。如果你更愿意使用 [ARM 内核和 Xilinx FPGA](https://hackaday.com/2018/10/02/free-arm-cores-for-xilinx-fpgas/)，这也是一个免费的——尽管不是开源的——选项。

 [https://www.youtube.com/embed/us2F8wAncw8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/us2F8wAncw8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

