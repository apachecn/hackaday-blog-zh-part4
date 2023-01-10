# 亲爱的，我缩小了 Arduino 核心

> 原文：<https://hackaday.com/2021/04/05/honey-i-shrunk-the-arduino-core/>

高级编程语言在简化程序员的工作方面做得很好，但是作为一种折衷，这些语言通常会降低效率。虽然一个普遍的想法是转向汇编这样的低级语言，以提高程序的速度或内存使用，但在采取这种极端做法之前，通常可以在高级别上做很多事情。当然，Arduino 平台也是如此，正如[NerdRalph]通过[缩小 Arduino 核心本身的大小](https://nerdralph.blogspot.com/2021/04/honey-i-shrunk-arduino-core.html)所展示的那样。

[NerdRalph]已经注意到“blink”示例程序实际上包含超过 1 kB 的无关代码，并且更复杂的程序包含更多的代码。为了解决这个问题，他创建了 ArduinoShrink，旨在使包含库更加模块化和独立。它修改了一些默认的寄存器和计数器，以使用更少的内存和提高速度，并且还旨在通过改变 Arduino 禁用中断的时间来改善中断延迟。

虽然 ArduinoShrink 有一些限制，例如需要在编译时知道关于管脚的细节，但对于任何为 Arduinos 编写内存密集型程序或需要改进计时的人来说，这可能是一个强大的新工具。但是，如果你想反其道而行之，避免学习 C 或汇编语言，[你可以一直在你的嵌入式设备上运行 Python](https://hackaday.com/2020/11/14/micropython-on-microcontrollers/)。