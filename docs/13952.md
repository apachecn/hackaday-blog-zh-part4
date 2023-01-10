# 基于 RP2040 的简单音频 DSP 板

> 原文：<https://hackaday.com/2022/06/21/a-simple-rp2040-based-audio-dsp-board/>

如果你是那些以制作音乐为目的而涉足电子产品的人之一，那么[DatanoiseTV]的这个基于 [Raspberry Pi RP2040 的音频 DSP 项目](https://github.com/DatanoiseTV/RP2040-DSP-FreeRTOS-Template)可能会感兴趣。提供了一个 FreeRTOS 模板应用程序，用于创建 Eurorack 兼容的合成器、效果处理器和类似的基于 DSP 的音频小部件。

[硬件平台](https://github.com/DatanoiseTV/RP2040-DSP-FreeRTOS-Template/tree/main/hardware)具有通常的 Eurorack 连接，包括 MIDI 输入、控制电压(CV)和通常的 5V 兼容触发器。提供音频输出，将音频发送到系统混音器或任何其他模拟模块。此外，还提供了旋转编码器、几个按钮和有机发光二极管显示器的连接，以便在需要时在模块上构建基本的用户界面。

应用程序模板足够通用，但是该项目旨在与 [Vult DSP transcompiler](https://github.com/vult-dsp/vult) 一起使用。Vult 是一种高级编程语言，旨在轻松创建音频合成器等，产生 C++代码作为编译过程的输出。然后，它与 RTOS 的好东西包装在一起(尽管你实际上并不需要它们),通过方便的 USB-C 端口以通常的方式放到 RP2040 上。因此，如果您正在寻找基于 DSP 的 Eurorack 模块用于您的家酿合成器机架，这可能是一个不错的起点。

就像 RP2040 不是 DSP 应用最明显的选择一样，[ESP32 也不是，但是谁在乎呢？如今，许多现代微处理器都具备音频 DSP 的能力，不管有没有专用功能。](https://hackaday.com/2019/05/24/eurorack-synth-module-runs-on-esp32/)