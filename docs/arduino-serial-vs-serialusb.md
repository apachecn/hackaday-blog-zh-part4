# Arduino 串口与串口总线

> 原文：<https://hackaday.com/2021/03/20/arduino-serial-vs-serialusb/>

[Andrew]想知道[为什么基于 Cortex M3 的 Arduino Due 上的`SerialUSB()`功能比 Uno 或 Nano 上的`Serial()`快这么多，并在这个短视频中分享了他的观察。他在两块板上画了一个简单的草图，然后用 Wireshark 评估结果。](https://www.youtube.com/watch?v=64qXT2zZmZM)

在基于 ATmega 的板上，数据以四个字符为一组在 USB 包中发送，但整个字符串都放在 Due 板上的一个包中。如果你看引擎盖下，答案就藏在显眼的地方。虽然 Arduino 系列主板使用 USB 虚拟串行端口连接到您的计算机，但 ATmega 主板上有一个实际的串行连接。例如，在 Nano 上，USB 连接器和微处理器之间有一个 FT232RL(在 Arduino Uno 板上，使用小型 ATMEGA8U2 代替 FTDI 芯片，但概念是相同的)。在 Arduino Due 上，USB 直接连接到 SAM3X8E 处理器。

当然，这个概念不仅仅适用于 Arduino 板。在两台计算机之间的任何串行连接中，当链路两端都使用虚拟 USB 设备时(不涉及实际的串行信号)，串行波特率是一个虚构的东西，数据传输速度仅取决于 USB。我们很好奇为什么在[Andrew]的 ATmega Wireshark 捕获中数据包包含四个字符——为什么不是 1、2 或 10 个？这是可以由程序员控制的，还是由协议和/或 FTDI 芯片固定的？如果你有答案，请在下面的评论中告诉我们。

 [https://www.youtube.com/embed/64qXT2zZmZM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/64qXT2zZmZM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

