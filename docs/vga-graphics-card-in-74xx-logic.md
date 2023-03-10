# 74xx 逻辑的 VGA 图形卡

> 原文：<https://hackaday.com/2021/04/30/vga-graphics-card-in-74xx-logic/>

我们推测，[Glen Kleinschmidt]怀着怀旧的心情，着手用分立逻辑芯片制造一个 640x480x64 VGA 控制卡。如果我们忽略 512Kx8 Cypress SRAM 视频存储器，他也成功了——而且是在可读性很强的[单页 A3 原理图](http://www.glensstuff.com/vgavideocards/schematic_card_b_version_2.pdf)上。目标是连接他的一些旧的 8 位机器，如 TRS-80 Model 1 和 BBC Micro，但现在他正在使用 20 多年前的 PIC16F877 micro 进行演示。

![](img/9b48a50838c346b4998b43d3a2bee29b.png)

[Glen]在他的网站上提供了所有的原理图、Gerbers 和 C 源代码，如果你想自己复制一个的话。他的作品中有三个版本，具有不同的功能(在他的网站上有一个表格)。作为一种替代方案，您可以始终使用 FPGA 或定制芯片(如 SSD1963)来为这些微处理器生成视频，但有时复古的冲动太强烈，无法抗拒。我们感觉对[格伦]来说，这是一个独立的项目，能够将其连接到他的 8 位计算机只是一个方便的借口。

这也不是[格伦]的第一个复古项目。看看他的[模拟计算机“弹跳球”项目](https://hackaday.com/2017/01/28/op-amps-combine-into-virtual-ball-in-a-box/)我们在 2017 年报道过。您是否曾纠结于构建还是购买的决策，您是如何决定的？

 [https://www.youtube.com/embed/PYd5TKs_X8s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PYd5TKs_X8s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

