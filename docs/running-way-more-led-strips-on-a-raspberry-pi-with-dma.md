# 使用 DMA 在树莓 Pi 上运行更多 LED 灯条

> 原文：<https://hackaday.com/2020/10/12/running-way-more-led-strips-on-a-raspberry-pi-with-dma/>

Raspberry Pi 是一款功能强大的紧凑型计算机，对各种项目都非常有用。然而，它缺少一些常见微控制器上的 IO 功能。这在运行可寻址 LED 灯串时最为明显。通常，这是使用 Pi 的 PWM 或音频输出来完成的，并且仅限于几个短字符串。然而，[【杰里米·P·边沁】已经找到了一种利用 Pi 的硬件来克服这些限制的方法。](https://iosoft.blog/2020/09/29/raspberry-pi-multi-channel-ws2812/)

诀窍是使用树莓 Pi 鲜为人知的[二级内存接口](https://iosoft.blog/2020/07/16/raspberry-pi-smi/)。SMI 硬件允许 Pi 使用直接存储器访问(DMA)将数据并行移出至 8 或 16 个 I/O 引脚，时序快速准确。这使得它非常适合产生信号，如 WS2812B LEDs 使用的信号，也称为新像素。

有了[Jeremy]的代码和合适的支持硬件，就可以从 Raspberry Pi 运行多达 16 个任意长度的 LED 灯条。[Jeremy]很好地概述了它的工作原理，涵盖了从 WS2812B LEDs 使用的数据格式到需要处理缓存以避免数据混乱的所有内容。黑客可以在所有 Pi 上工作，从不起眼的 Pi 0 到强大的 Pi 4。由于使用了 DMA，这种技术不会使 CPU 过载，所以性能应该会很好。

当然，还有其他方法来驱动一吨的 LEDs 例如，我们见过 20，000 人在 ESP32 上跑步。

【感谢 Petiepooo 的提示！]