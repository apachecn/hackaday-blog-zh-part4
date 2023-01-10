# Xilinx 使 MIPI CSI 和 DSI 控制器 IP 模块可免费用于 Vivado

> 原文：<https://hackaday.com/2020/06/09/xilinx-makes-mipi-csi-and-dsi-controller-ip-blocks-free-to-use-with-vivado/>

如果你想在 FPGA 上使用显示器或摄像头，你通常会选择基于 MIPI 的解决方案。自 Xilinx Vivado 2020.1 版本起，MIPI DSI(显示器串行接口)和 CSI(摄像机串行接口)IP 模块现已与 IDE 捆绑在一起，可与 Xilinx FPGAs 一起自由使用。

[Xilinx MIPI CSI2](https://www.xilinx.com/products/intellectual-property/ef-di-mipi-csi-rx.html) 接收器模块实现了 [CSI-2 v1.1](https://en.wikipedia.org/wiki/Camera_Serial_Interface) 规范，虽然稍旧，但本质上与 Raspberry Pi 板上的 CSI 实现相同。这意味着它允许在 FPGA 上使用这个 IP 模块，并带有许多常见的 CSI 摄像头模块。IP 模块提供了一个标准的 [AXI4](https://en.wikipedia.org/wiki/Advanced_eXtensible_Interface) 接口，用于连接设计的其余部分。

类似地， [Xilinx MIPI DSI](https://www.xilinx.com/products/intellectual-property/ef-di-mipi-dsi-tx.html) 变送器模块执行 [DSI v1.3](https://en.wikipedia.org/wiki/Display_Serial_Interface) 规范。这提供了 1.5 Gbps 的最大数据速率，利用 AXI4-lite 接口与设计的其余部分进行通信。这两个知识产权块都受[核心许可协议](https://www.xilinx.com/products/intellectual-property/license/core-license-agreement.html)的约束，这似乎并不排除它被用于特定的方式，无论是商业还是个人。

当然，这不是在 FPGA 上使用 MIPI 器件的唯一方式。以[Daveshah]在 Github 上的 [CSRIx 项目为例。](https://github.com/daveshah1/CSI2Rx)

标题图像:Kwapix / [CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:Xilinx_XC3090-70_FPGA.jpg)