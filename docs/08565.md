# 带有自定义 PID 的 FTDI VCP 芯片在 MacOS 11 Big Sur 上不工作

> 原文：<https://hackaday.com/2020/12/03/ftdi-vcp-chips-with-custom-pids-not-working-on-macos-11-big-sur/>

一位匿名读者向我们提出了一个问题，这个问题会影响那些从苹果花园跳到最新最好的操作系统的人: [USB 设备由于基于 FTDI 的 USB 解决方案](https://www.ftdicommunity.com/index.php?topic=547.0)而停止工作。其核心似乎是苹果公司提供的内置 FTDI 驱动程序(AppleUSBFTDI.dext)只支持提供标准 FTDI 供应商和产品 ID(例如 FT232R 分别为 0x0403 和 0x6001)的 FTDI 芯片。然而，许多产品设置了自定义产品 ID (PID)来区分他们的设备，尽管在帖子中有些人提到即使默认的 VID/PID 组合也存在驱动程序问题。

在过去的几年里，Apple 一直在限制和改变内核扩展(KExt)和驱动程序扩展(DExt)的处理方式。由于这些 FTDI 芯片通常用于虚拟 com 端口(VCP)，如 Arduino 板和 USB-TTL 适配器，这是一个相当麻烦的问题，会影响任何将 Big Sur 与这样的硬件设备结合使用的人。

到目前为止，只有 FTDI 团队在支持论坛的帖子上有所回应，而苹果似乎对这个问题保持沉默。