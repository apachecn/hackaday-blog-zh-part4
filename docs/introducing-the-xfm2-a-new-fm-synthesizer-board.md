# 介绍 XFM2:新型 FM 频率合成器板

> 原文：<https://hackaday.com/2020/02/22/introducing-the-xfm2-a-new-fm-synthesizer-board/>

[René Ceballos]联系我们关于[新 XFM2 FM 合成器板](https://www.futur3soundz.com/xfm2)，它是我们去年在 Hackaday 报道的 XFM [的继任者。除了将 FPGAs 从 Spartan 6 更改为 Artix-7 35，DAC 也从 16 位升级到 24 位。由于该项目基于两个易于获得的 FPGA 和 DAC 功能板，因此任何人都可以轻松地重新创建。![https://images.squarespace-cdn.com/content/v1/5d2c7309e3281e0001ef5655/1580208742008-DDG6FHLVST9DTOU5YDV7/ke17ZwdGBToddI8pDm48kIzPiMR3_Rs2gge4hyoameUUqsxRUqqbr1mOJYKfIPR7LoDQ9mXPOjoJoqy81S2I8N_N4V1vUb5AoIIIbLZhVYxCRW4BPu10St3TBAUQYVKc8LXFP3nIOov1DiYlxUpn2kjauiJB9jSbs9pkYnnzvQkOGqqUmgmVAUPjW85v7F78/xfm2.PNG?format=1500w](img/3abdb70b323e1683c7da62ce3a977d9b.png)](https://hackaday.com/2019/07/24/xfm-a-32-voice-polyphonic-fm-synthesizer-on-an-fpga/)

该项目由一个具有光隔离 MIDI 输入端口的下板、一个 24LC1025 EEPROM 和几个无源器件组成，其上安装了基于 [Adafruit](https://www.adafruit.com/product/3678) [UDA1334A](https://www.nxp.com/pages/low-power-audio-dac-with-pll:UDA1334) 的 I2S 解码板和一个 [Digilent Cmod A7-35T](https://store.digilentinc.com/cmod-a7-breadboardable-artix-7-fpga-module/) ，包含 Xilinx[xc7a 35t-1 CpG 236 c](https://www.digikey.com/product-detail/en/xilinx-inc/XC7A35T-1CPG236C/122-1907-ND/5039071)Artix-7 FPGA。[René]在 XFM2 页面上提供了原理图和 BOM。零件总成本应该在 99 美元左右。

用户手册、安装指南和必须加载到 FPGA 中的二进制文件(使用所提供的说明)都是可用的。不幸的是，没有提供 HDL 源，但这不应该剥夺像这样组装 FM 合成器板的乐趣。

[René ]表示，根据对 XFM 项目的反馈，他现在正在为董事会设计一个可视化用户界面。一旦这一切都运转正常，并取决于 XFM2 用户的反馈，他可能会决定开始一场众筹活动。