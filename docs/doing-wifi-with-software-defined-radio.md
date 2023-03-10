# 使用软件无线电实现 WiFi

> 原文：<https://hackaday.com/2021/01/16/doing-wifi-with-software-defined-radio/>

软件定义无线电允许 RF 硬件承担多种任务，这完全取决于硬件在代码中的使用方式。bladeRF 2.0 micro xA9 就是这样一款设备，它封装了一个胖胖的 FPGA，为板上的信号处理链提供了充足的空间。为了展示其能力， [[Robert Ghilduta]着手为该平台编写软件定义的 WiFi 实现。](https://www.nuand.com/bladeRF-wiphy/)

这项工作被称为 bladeRF-wiphy，因为它在 7 层 OSI 网络模型中实现了 phy，即 WiFi 连接的物理层。WiFi 信号的调制和解调全部由 Cyclone V FPGA 板载处理，解码后的 802.11 WiFI 数据包移交给 Linux mac80211 模块，该模块处理 mac 层或媒体访问控制。由于 mac80211 内置的功能，该系统可以根据手头的任务充当接入点或单独的工作站。

[Robert]很好地解释了在 FPGA 上实现 WiFi 调制的原因和方法，以及软件和硬件中调制解调器开发的一些基础知识。这是一个密集的东西，所以对于软件无线电领域的新手来说，[考虑参加一些课程来让自己跟上速度吧！](https://hackaday.com/2020/07/08/software-defined-radio-academy-goes-virtual/)