# IBM 发布基于 OpenPOWER ISA 3.1 规范的 POWER10 CPU

> 原文：<https://hackaday.com/2020/08/19/ibm-reveals-power10-cpu-based-on-the-openpower-isa-3-1-specification/>

本周，IBM [发布了](https://newsroom.ibm.com/2020-08-17-IBM-Reveals-Next-Generation-IBM-POWER10-Processor)他们的 [POWER10](https://en.wikipedia.org/wiki/POWER10) CPU，这看起来可能不太令人兴奋，因为它主要针对大型主机和服务器。对大多数人来说，真正的消息是它是第一款基于开放的 [Power ISA](https://en.wikipedia.org/wiki/Power_ISA) 规范 3.1 版的处理器。Power ISA 的这个新版本增加了许多新指令以及可选性的概念。它更新了 2015 年发布的 3.0 版规范，就在 [OpenPOWER Foundation](https://en.wikipedia.org/wiki/OpenPOWER_Foundation) 成立之后。

目前，存在许多 Power ISA 的开源设计，包括[微瓦](https://en.wikipedia.org/wiki/OpenPOWER_Microwatt) (Power v3.0，VHDL)和类似的 ChiselWatt(用基于 Scala 的 Chisel 编写)。今年 6 月，IBM 还在 [Github](https://github.com/openpower-cores/a2i) 上发布了 [IBM A2](https://en.wikipedia.org/wiki/IBM_A2) 处理器的 VHDL 代码。这是一款支持多核的 4 路多线程 64 位设计，芯片实现运行频率高达 2.3 GHz，使用 Power ISA v2.06 规范。

ISA 规范和其他相关技术文档可以从 [OpenPOWER](https://openpowerfoundation.org/) 网站获得，例如从 2017 年开始的 [Power ISA v3.0B 规范](https://openpowerfoundation.org/?resource_lib=power-isa-version-3-0)。该网站还列出了围绕 Power ISA 的[当前核心和社区](https://openpowerfoundation.org/cores-and-more/)。

(主图:POWER10 CPU，credit IBM)