# Remoticon 2021: Uri Shaked 反转 ESP32 WiFi

> 原文：<https://hackaday.com/2021/12/30/remoticon-2021-uri-shaked-reverses-the-esp32-wifi/>

你知道当你在做一个项目时，其他的支线任务会在左右弹出吗？您可以选择简要地处理它们，或者您可以将它们作为独立的项目来深入研究。Uri Shaked 是 wok wi T1 的作者，这是一个在线 Arduino 模拟器，允许你在模拟硬件上测试你的代码。(非常非常爽。)在过去，Arduino 的意思是 AVR，他在[逆向工程芯片](https://hackaday.io/course/176685-avr-architecture-assembly-reverse-engineering)上投入了一些令人敬畏的努力，以便成功地模拟它。但是现在“Arduino”不仅仅意味着 AVR，所以 Uri 必须解决 STM32 ARM 芯片和[甚至最近的 RP2040](https://hackaday.io/course/178733-raspberry-pi-pico-and-rp2040-the-deep-dive) 。

Arduino 也运行在 ESP32 上，所以 Uri 戴上了他的逆向工程帽子(字面意思)并瞄准了那个芯片。但是，ESP32 比其他任何微控制器都要复杂得多，不仅基于稍显小众的 Xtensa 芯片，还具有板载 WiFi 及其相关的二进制固件。对 ESP32 的 WiFi 进行逆向工程是 Uri 着手进行的附带任务，完全粉碎了，并且[在这个杰出的 Remoticon 2021 演讲](https://www.youtube.com/watch?v=XmaT8bMssyQ)中为我们记录了这些。

## 偷看和戳戳

ESP32 将 WiFi 视为内存映射外设，就像您可能习惯的微控制器一样。例如，对于 GPIO 引脚，内存映射意味着您可以将 1 或 0 写入内存的特定位，它将打开或关闭外部 LED。从那个存储单元读取，你可以知道是否有人按了一个按钮。对于 WiFi 来说，基本上是一样的，只是它几乎完全没有记录内存地址在哪里以及它们的用途。Uri 的方法使用一个调试器来调试物理硬件上的 JTAG，一个 Ghidra 插件来帮助他处理二进制文件，以及他自己的 ESP32 模拟器来找出所有这些。

首先，他将一个简单的 ESP-IDF WiFi“hello world”程序闪入他的模拟器，将日志记录的冗长度提高到 11，并运行它，直到它崩溃。它做得很快，因为他的模拟器还没有模拟任何 WiFi 硬件。借助调试器 GDB，他可以找出哪个函数崩溃了。然后他把那个功能拆开了。

从一开始，他就走运了。一个被称为`hal_mac_deinit()`的函数，除了将特定的值写入固定的内存地址，并等待特定的响应之外，似乎没做什么。然后他编程他的模拟器来给出那个响应，这使得程序在下游崩溃了一点点。成功！问题中的内存地址映射到什么？数据表上写着“保留”,但这并不需要太大的信心来假设它是某种 WiFi 控制寄存器。

演讲的其余部分由尤里解释了在他的模拟器上崩溃的程序之间的反复切换，使用吉德拉和 GDB 来找出崩溃的代码做了什么，然后将期望的行为集成到他的模拟器中，直到那段代码工作为止。真正令人惊讶的是，这最终模拟了 ESP32 的 WiFi 在内部是如何工作的，这是如此之好，以至于他可以在模拟的设备上运行 Python MQTT 库，并且它完全像在本地硬件上运行一样工作。太神奇了！

这是一个很棒的演讲，提供了使用仿真作为关键工具的逆向工程的高级概述。这是一个伟大的技术，我们很高兴能够看到尤里隐喻的肩膀。看看吧！

 [https://www.youtube.com/embed/XmaT8bMssyQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XmaT8bMssyQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

