# 最小 TinyAVR 0 编程

> 原文：<https://hackaday.com/2020/10/05/minimal-tinyavr-0-programming/>

当[Alain]想要使用一些新的 TinyAVR 0 芯片时，特别是 Attiny406，使用 Windows IDE 似乎有些过头了。关于使用简单的命令行工具对其他 AVR 芯片进行编程，有大量的信息来源，但对于这些使用一种称为 UPDI 的新编程协议的较新的 0 系列器件却没有。这导致了对如何使用文本编辑器、makefile 和 USB 转串行电缆对 TinyAVR 0 进行编程的深入研究。

Attiny406 具有闪存 4K 和 256 字节 RAM，无需外部时钟即可以 20 MHz 的速度运行。你可能会认为编程类似于常规 AVR 器件，但这些微型器件使用 UPDI(统一编程和调试接口),它使用 3 个引脚进行编程。旧设备使用不同的协议。

创建一个 UPDI 程序员是非常容易的。只需一根 USB 至逻辑电平串行电缆和一个 4.7K 电阻。还有知道如何驱动协议的 [Python 代码](https://github.com/mraardvark/pyupdi)。您还可以使用 Raspberry Pi 上的逻辑级串行端口，对设备树进行一些修改，这在代码的文档中有解释。

[Alain]为设备制作了一个漂亮的[分线板。它适合试验板，允许 5V 或 3.3V 工作，并有一个 LED 和开关。没什么特别的，但是很方便。一旦你知道如何将一个十六进制文件装载到芯片上，剩下的就很简单了。虽然 AVR 版本的 gcc 不支持开箱即用的交叉编译，但 Microchip 的](https://aisler.net/omzlo/playground/attiny406-dev)[设备包](http://packs.download.atmel.com)支持该功能。

趋势是走向更大的处理器，而不是更小的，但是当你需要在一个小空间里塞满一些东西，每单位节省几便士，或者消耗非常少的功率时，这些微小的处理器可以是正确的选择。处理器可能很小，但是如果你工作的话，你可以用它们做[一些相当大的事情。](https://hackaday.com/2020/01/07/tiny-machine-learning-on-the-attiny85/)