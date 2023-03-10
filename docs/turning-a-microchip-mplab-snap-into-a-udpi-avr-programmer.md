# 将微芯片 MPLAB Snap 转变为 UDPI AVR 编程器

> 原文：<https://hackaday.com/2022/12/26/turning-a-microchip-mplab-snap-into-a-udpi-avr-programmer/>

统一编程和调试接口(UPDI)是 Microchip 用于编程和片上调试的专有接口，在 Microchip 收购 Atmel 之后，已经成为 AVR MCUs 上的标准。作为一个专有接口意味着即使像 Atmel-ICE 这样的入门级程序员也相当昂贵，超过 100 美元。对于[斯科特·W·哈登]来说，这时候就出现了一个问题，便宜得多的 MPLAB Snap 板(～34 美元)[是否也可以用于 AVR UDPI 目的](https://swharden.com/blog/2022-12-09-avr-programming/)。

[Scott]在使其工作之前经历的痛苦阶段包括更新 MPLAB Snap 板固件，在试图使用 Snap 进行 AVR MCU 编程时被 Microchip Studio IDE 责骂，以及最终按照相关的 Microchip 工程技术说明( [ETN #36](http://ww1.microchip.com/downloads/en/DeviceDoc/ETN36_MPLAB%20Snap%20AVR%20Interface%20Modification.pdf) )修复板，该说明规定移除 Snap 板上的 4.7kω下拉电阻(R48)。这允许 MCU 将 UDPI 线拉高。

正如 ETN 指出的，外部上拉也可以用来覆盖下拉，这将使快照的 ICSP 功能保持不变。正如[Scott]在他的结论中提到的，似乎 Snap 对 UDPI AVR 的支持实际上是 Microchip 的一个补充。同时，正如[Scott]所补充的，也有更多的 DIY 解决方案，它们对于仅仅刷新 MCU 是有用的。USB-TTL 串行适配器和 pymcuprog 就是一个例子。

像 [jtag2updi](https://hackaday.com/2022/04/15/this-diy-updi-programmer-is-nice-and-cheap/) 、 [ftdi2updi、](https://teddywarner.org/Projects/SerialUPDI/)及其同类 DIY 解决方案的问题是组装它们所需的工作，以及随着 updi 生态系统随着新设备和新功能的不断发展而长期支持的不确定性。带有电阻模块 MPLAB Snap 可能只是 Atmel-ICE 和逆向工程 OSS 项目之间的中间地带。

(特色图片:MPLAB Snap 电阻器模型图解，来自[微芯片 ETN #36](http://ww1.microchip.com/downloads/en/DeviceDoc/ETN36_MPLAB%20Snap%20AVR%20Interface%20Modification.pdf) )