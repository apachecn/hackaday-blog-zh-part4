# 嵌入式仪表板明确显示数据

> 原文：<https://hackaday.com/2022/07/15/embedded-dashboard-definitely-displays-data/>

我们经常会发现自己在使用一台连接到项目的 PC 进行串行调试。其他时候，我们会眯着眼睛盯着状态指示灯，试图记住我们发明的闪烁代码。[这款来自【hgrodriguez】](https://github.com/hgrodriguez/embedded-dashboard-console)的嵌入式仪表盘旨在达到中间的某个位置。

仪表板上有发光二极管，几个 5×7 矩阵显示器，还将安装一个小型有机发光二极管显示器。板上的一切都由 ItsyBitsy 板驱动，该板具有 Atmega32u4 微控制器。数据可以通过 UART、SPI 或最终通过 I2C 馈入 ItsyBitsy。

由于 ItsyBitsy 处理实际上驱动了各种显示，您的项目只需要通过列出的接口之一发送调试数据。然后，ItsyBitsy 将在矩阵显示器上显示您的字节值或字值，根据需要使 led 闪烁，等等。

其结果是一个有用的小控制台，可以显示你的微控制器项目的大脑中正在发生什么。它不能代替[全串行终端](https://hackaday.com/2019/12/28/a-pocket-sized-terminal-for-mobile-python-hacking/)，但当你需要查看 RAM 中的一些变量时，它肯定会派上用场！