# 适用于任何项目的 USB-C 可编程电源

> 原文：<https://hackaday.com/2021/01/16/usb-c-programmable-power-supply-for-any-project/>

USB-C Power Delivery 3.0 (PD3.0)引入了新的可编程电源(PPS)模式，允许器件以 20 mV 步长协商 3.3-21 V 的任何电源，并以 50 mA 步长协商最高 5 A 的电流。为了利用这一新标准，[Ryan Ma]创建了 [PD Micro](https://hackaday.io/project/176680-pd-micro-usb-c-pd30-pps-trigger) ，这是一个 Arduino 兼容开发板和一个独立的软件库，允许将 PD3.0 和旧的 PD2.0 轻松集成到项目中。

开发板围绕 ATMega32U4 微控制器和 FUSB302 USB-C PHY 构建。四层 PCB 两侧密集封装，适合 Arduino Pro 微型外形。该板可以从适当的电源提供高达 100W (20 V，5 A)的功率，并通过一组 led 显示 PD 状态的视觉反馈。

项目的首要目标实际上是在软件中。[Ryan]发现现有的用于 PD 的软件库占用大量内存，并且难以集成到小型项目中。根据 PD 规格和 PD PHY 芯片数据手册，他创建了一个重量更轻、功能完备的软件库，消耗不到 8 K 的闪存和 1 K 的 RAM。这还不到 ATmega32U4 上可用闪存和 RAM 的一半。

[Ryan]正在进行一场[大众供应活动](https://www.crowdsupply.com/ryan-ma/pd-micro)(休息后的视频)以将这些强大的电路板放在野外，并在 GitHub 上发布了所有的[源代码和原理图。PCB 设计文件将在活动的最后一周发布，大约在 2021 年 1 月 25 日。](https://github.com/ryan-ma/PD_Micro)

[USB-C 和电源传输](https://hackaday.com/2018/08/17/the-wonderful-world-of-usb-type-c/)并不是简单的标准，但将高速数据接口和[可编程电源](https://hackaday.com/2020/10/23/a-plethora-of-power-delivery-potential/)添加到几乎任何项目中的能力都具有真正的潜力。

[https://player.vimeo.com/video/491774506](https://player.vimeo.com/video/491774506)