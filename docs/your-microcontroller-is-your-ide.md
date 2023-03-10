# 您的微控制器就是您的 IDE

> 原文：<https://hackaday.com/2020/07/05/your-microcontroller-is-your-ide/>

如果你的微控制器 IDE 是在微控制器本身上运行，而不是在你用来编程的计算机上运行，那会怎么样？Arduino 最大的遗产可以说是软件方面的，因为它用一个可以在一系列操作系统上轻松安装、易于使用，最重要的是，*可以工作*的环境取代了恼人的专有开发环境。可移植性下一个层次是摆脱任何专门的计算机端软件。[Ronny Neufeld]为 ESP32 编写了一个可通过 web 浏览器访问的微 IDE，有趣的是，它托管在目标设备本身上。

使用 IDE 非常简单，安装一个二进制文件，用 web 浏览器连接到 ESP，开始编写 MicroPython 代码。可以选择直接连接到芯片作为热点，或者通过另一个 WiFi 网络连接。界面看起来相当光滑，但他煞费苦心地提醒我们，这是一项正在进行中的工作。遗憾的是，目前还没有源代码，因为这是一个非商业用途的免费二进制发行版，我们希望有一天会有一个开源版本。这并不适合所有人，但从几乎任何现代设备访问相同界面的便利应该有助于吸引一个健康的社区。

这似乎是我们向您展示的第一个基于网络的片上 ESP IDE。但这不是第一个片上编码的例子，[正如这个基本解释器显示的](https://hackaday.com/2016/10/27/basic-interpreter-hidden-in-esp32-silicon/)。

[主图像来源:Ubahnverleih / [CC0](https://commons.wikimedia.org/wiki/File:ESP32_Espressif_ESP-WROOM-32_Dev_Board.jpg) ]