# XFM:FPGA 上的 32 声部复音调频合成器

> 原文：<https://hackaday.com/2019/07/24/xfm-a-32-voice-polyphonic-fm-synthesizer-on-an-fpga/>

调频(FM)合成器芯片吸引了大量观众。这就是[ 勒内·塞瓦洛斯 ]的 [XFM 项目](https://www.futur3soundz.com/)背后的原因之一，该项目旨在 FPGA 上复制过去的纯 FM 合成器芯片的声音，如雅马哈 DX 系列、OPL 芯片系列和 TX81Z/802/816。结果是一个复音，32 个声音，6 运营商调频合成器立体声模块。

项目页面详细介绍了最终导致 XFM 在 FPGA 上实现的设计选择，而不是使用专用 DSP 或 MCU。[]勒内 ]来自在个人电脑上运行的虚拟合成器的世界，他的第一个想法是在树莓 Pi 或类似的设备上实现一些东西。不幸的是，这些电路板需要大量的电力(排除了电池供电的操作)，并且几乎不能被称为实时的，这导致[ René ]放弃了这一尝试。

反对使用 MCU 的设计选择很简单:虽然能够进行实时处理，但它们缺乏必要的功率，因此不适合音频处理。通过计算来确定需要什么样的处理能力，发现大约需要 650 MIPS，这个数字是大多数 MCU 努力实现的一部分。

由于对 XFM 的进一步要求之一是它应该尽可能便宜，这就排除了具有所需功能和硬件特性的 DSP 芯片过于昂贵的可能性。选择的元件是 Xilinx Spartan 6 FPGA，虽然在 FPGA 领域有些声名狼藉和被回避，但对于这个项目来说，它是一个非常经济的选择。

选择了具有 16 个 DSP 模块的 Spartan 6 XC6SLX9 作为平台的 [Mojo V3](https://alchitry.com/products/mojo-v3) ，【 René 】然后创建了用于 MIDI 和 SPDIF 接口的附加板，以及用于程序存储器的 EEPROM 和使用分立元件实现的双σ-δ16 位 DAC。

结果是相当令人印象深刻的，因为你可以听到自己在下面包括的视频，并简要看看 XFM 系统的行动。

作为一种开放的设计，设计文件和软件可以通过网站提供给任何想要构建自己的 XFM 系统的人，前提是他们可以使用当前支持的 FPGA 板的位文件。不幸的是，Mojo V3 板在这一点上已经被淘汰，但[ René ]在给我们的回复中表示，他已经将 HDL 移植到了 [Numato Mimas](https://numato.com/product/mimas-spartan-6-fpga-development-board) 和 [CMOD A7](https://store.digilentinc.com/cmod-a7-breadboardable-artix-7-fpga-module/) 板上，并将在几周内提供这些平台的位文件。

有传言说，未来可能会为定制板甚至 ASIC 版本进行众筹，这就是不开源 HDL 的原因。

 [https://www.youtube.com/embed/yuGaNpHQpoo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yuGaNpHQpoo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

