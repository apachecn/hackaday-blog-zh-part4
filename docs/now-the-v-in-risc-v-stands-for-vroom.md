# 现在 RISC-V 中的 V 代表 VRoom

> 原文：<https://hackaday.com/2022/03/26/now-the-v-in-risc-v-stands-for-vroom/>

如今，用 HDL 编写的数百种开源 CPU 似乎在互联网上到处流动(这是一件好事)。许多是 RISC-V，一种开源指令集(ISA)，是对学习和小任务有用的小玩具处理器。然而，如果你是[保罗·坎贝尔]，你会选择一个被称为 VRoom 的 RISC-V CPU 的[高端超标量、无序、投机、8 IPC 怪物！](https://moonbaseotago.github.io/)。

对于处理器设计领域的门外汉来说，这可能看起来有点像单词汤(公认相对较小)，但这与 [VexRISC](https://hackaday.com/2017/07/21/vexriscv-a-modular-risc-v-implementation-for-fpga/) 的不同之处在于规模和复杂性。它不是一次按顺序执行一条指令，而是执行多条指令，以它能处理的任何顺序同时完成它们。VexRISC 芯片是一个很好的 32 位模块化设计，可以运行 Linux。在一切都开启的情况下，它拉起了稳定的 1.57 [DMIPS/MHz](https://electronics.stackexchange.com/questions/517114/what-is-dmips-mhz) 。VRoom 已经以 6.5 DMIPS/MHz 的速度运行，性能提升更多。它在每个时钟周期达到 8 条指令的峰值，有一个双寄存器文件和一个智能提交系统来跟上。

VRoom 是在系统 Verilog 中编写的，以利用 Verilator(一个方便的林挺和模拟框架)，虽然有一些 C 可以生成不同的文件，但我们敢打赌，与基于[类型脚本的项目](https://hackaday.com/2021/10/14/risc-v-in-typescript/)相比，它是非常普通的。VRoom 目前通过 AWS-FPGA 实例(Xilinx VU9P Ultrascale)启动 Linux，尽管它必须进行调整才能适应。[Paul]有一个宏大的计划，要开发一款服务器级的芯片，拥有许多内核和巨大的高速缓存。

这一切都在 GPLv3 许可下的 GitHub 上进行；去看看！【保罗】还有[有一个关于很多重要细节的演讲](https://moonbaseotago.github.io/talk/index.html)。如果你对 RISC-V 感兴趣，但服务器级不是你的速度，我们听说 Espressif[开始在他们一直受欢迎的 ESP 系列](https://hackaday.com/2021/08/04/new-part-day-an-esp-with-zigbee/)中使用 RISC-V 内核。