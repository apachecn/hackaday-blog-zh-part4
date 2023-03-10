# Xilinx 上的免费 ARM 内核入门

> 原文：<https://hackaday.com/2018/12/04/getting-started-with-free-arm-cores-on-xilinx/>

我们之前报道过 Xilinx 提供免费使用的 ARM Cortex M1 和 M3 内核。[Adam Taylor]发布了他让事情运转起来的[经验](https://www.element14.com/community/blogs/Exploring_the_Programmable_World/2018/11/19/getting-up-and-running-with-arm-design-start)，还有一个由[Geek Til It Hertz]根据你在下面第二个视频中看到的材料制作的视频。

本文介绍了 Arty A35T 或 Arty S50 FPGA 板(基于 Artix FPGAs)和 Xilinx Vivado 软件的使用。虽然 Vivado 将允许您进行传统的 FPGA 开发，但它也可以组合功能块来生产 CPU，这就是这里正在发生的事情。

最终的设计有一个 M3 处理器、一条 AXI 总线、一个 UART、一些 GPIO、一个调试器和一些 RAM。你用一个类似示意图的图表来操作这些部分。最后，您可以使用 PC 上的串行端口和终端程序连接到该设备。

你仍然需要为你的新 CPU 做软件开发，[亚当的]承诺这是他的帖子的第二部分，他将很快发布。然而，这通常是人们没有那么多麻烦的部分。此外，您可能有自己喜欢的、无论如何都想使用的 ARM 开发工具。

我们之前讨论过这些内核的[免费可用性，最好有一个快速的分步指南。如果你不使用 Xilinx，你可以考虑另一种 CPU，如](https://hackaday.com/2018/10/02/free-arm-cores-for-xilinx-fpgas/) [RISC-V](https://hackaday.com/2017/10/04/sifive-announces-risc-v-soc/) 或 [NIOS-II](https://hackaday.com/2018/10/05/easy-fpga-cpu-with-max1000/) 。

 [https://www.youtube.com/embed/51r47K0H5uw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/51r47K0H5uw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/fxsgE5ZfrvQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fxsgE5ZfrvQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

