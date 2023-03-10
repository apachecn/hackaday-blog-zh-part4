# 用裸 C 语言进行 ARM 编程

> 原文：<https://hackaday.com/2018/08/21/arm-programming-with-bare-c/>

我们忏悔。当开始一个微控制器项目时，我们通常从我们为该环境所做的最后一个项目开始，复制它，并进行更改。第一个呢？它——咳咳——可能是在网上找到的。这不仅仅是你的代码。如果您想亲自完成(并理解)ARM 开发项目中的所有事情，您可以使用一体化演练。碰巧[Jacob Mossberg]有一本从头开始的指南，指导你如何让你的 C 代码在 ARM 上运行。

从一个 ARM Cortex M3 开始，他编写了一个简单的 C 程序，并得到了等价的汇编语言。接下来是对机器码的详细分析，探索编译器假设将要设置的内容。这有助于理解启动代码和链接器脚本应该是什么样子。

这是一个很好的方法，让我们想起了一句老话“授人以鱼”他甚至花了一点时间谈论如何使用 OCD 进行调试。当然，具体细节取决于他使用的芯片，但大部分内容适用于任何 ARM 芯片。即使你不使用 ARM，思维过程和方法本身也是非常有趣的。

如果你正在使用蓝色药丸，并准备离开 Arduino 生态系统，这篇文章将会是一个很好的选择。当然，如果你想远离 Arduino 系统，但不想完全依赖裸机，总有 [mBed](https://hackaday.com/2017/04/07/platformio-and-visual-studio-take-over-the-world/) 。