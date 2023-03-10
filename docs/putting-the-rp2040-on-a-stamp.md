# 将 RP2040 贴在邮票上

> 原文：<https://hackaday.com/2022/03/28/putting-the-rp2040-on-a-stamp/>

在电子世界中，一个 1 英寸见方、边缘呈齿形的小电路板可以在很小的表面区域内轻松添加大量电路。你可以抓住一个预先组装好的模块，把它扔到你选择的 PCB 上，这样可以节省很多布线和焊接的时间。来自[SolderParty]的这个[小树莓 Pi 2040 模块](https://github.com/solderparty/rp2040_stamp_hw)勾选了所有这些框。

凭借所有 30 个 GPIO、8MB 板载闪存和一个 NeoPixel 板载，在 RPi2040 已经令人印象深刻的规格之上，您还有很多可以玩的。在线程序员的时代已经一去不复返了，它使用一个 UF2 引导程序来使通过 USB 传输新图像变得容易。Rust、MicroPython、Arduino 和 PicoSDK 都是代码的开发选项。所有的 KiCad 文件、BOM、原理图和固件都在 CERN 许可下的 GitHub 上，供您阅读。它们包含了有益的尺寸和参考载板设计。

这是一个方便的小项目，可能值得记住，或者只是作为您工作的参考设计。从 STM 的角度来看，我们对 RPi2040 有一个很好的概述。如果你想知道你甚至可以用这个小邮票做什么，[为什么不驱动 HDMI 信号](https://hackaday.com/2021/02/12/bitbanged-dvi-on-a-raspberry-pi-rp2040-microcontroller/)？