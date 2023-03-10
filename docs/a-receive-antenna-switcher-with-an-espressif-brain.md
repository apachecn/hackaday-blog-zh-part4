# 一种具有表情大脑的接收天线切换器

> 原文：<https://hackaday.com/2022/05/21/a-receive-antenna-switcher-with-an-espressif-brain/>

对于一个无线电发烧友来说，同一台无线电有多个天线并不罕见，所以正如你可能会想到的那样，有一堆同轴电缆悬挂下来以便在钻机后面摸索交换也是完全正常的。如果这描述了你的无线电体验，那么你可能会对[g3gg0] 制造的[天线切换器感兴趣，它使用由 ESP32 模块控制的固态 RF 开关。](https://www.g3gg0.de/wordpress/rf/an-esp32-based-rf-antenna-matrix/)

其核心是 [MXD8625C](https://lcsc.com/product-detail/RF-Switches_Maxscend-MXD8625C_C285546.html) RF 开关，这是一种专为手机应用设计的微型设备，仅提供一小部分 dB 的插入损耗，并且在某种程度上不需要任何隔直电容。它由 GPIO 线控制，他连接了一对天线，允许将三个天线分配给几个无线电设备，如果需要，可以方便地选择切换到前置放大器。更有趣的是，我们注意到该器件也适合发射机开关，最大吞吐量为 36.5 dBm，我们计算出其吞吐量约为 4.5 W，该板显然适合接收应用，但考虑收发器项目的人可能会对该芯片感兴趣。同时，该软件是一个相对简单的基于网络的控件，将屏幕上的控件链接到 GPIOs。

如果你对固态 RF 开关感兴趣，请记住[在较低频率下，它们可能非常简单](https://hackaday.com/2021/10/24/is-a-diode-a-switch/)。