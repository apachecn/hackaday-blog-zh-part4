# C64 在 STM32F429 Discovery 上运行

> 原文：<https://hackaday.com/2020/11/18/c64-runs-on-stm32f429-discovery/>

这些年来，Commodore C64 有过各种各样的重生，而[Dave Van Wagner]创造了一个可以在 STM 32 f 429 zi Discovery 开发板上运行的版本。这些开发板已经存在好几年了，除了典型的 I/O 电路之外，还配有 2.4 英寸彩色 TFT LCD，非常超值— [Dave]说它们目前的分销价格不到 30 美元。

该项目始于今年早些时候，当时[Dave]着手用 C#编写一个模拟 C64 Basic 的命令行程序。许多年前，他编写了一个 6502 仿真器，但是没有测试过。[Dave]在三月份进行了一次编程狂欢，并在一个很长的周末让它运行起来。他随后决定增加对 VIC-20、TED 和 PET 的支持。

尽管[Dave]说 C#是一种美丽的语言，但他随后将程序移植到了 C(一种丑陋的语言？)以便在发现板上运行，将命令行终端接口换成真正的 LCD 视频和 USB 键盘。还有一个 Arduino 版本(仅终端接口)。它的运行速度比真正的 C64 慢 15%,而且还有一些限制，比如没有 SID。但总的来说，这是一个伟大的项目，也是以嵌入式格式模拟 C64 的低成本方式。如果你想进一步探索，这里有 STM32F429 的 [Mbed 项目，你可以在他的](https://os.mbed.com/users/davervw/code/C64-stm429_discovery/) [GitHub 页面](https://github.com/davervw)找到 Arduino 和 C#版本。你可能还记得我们去年报道过的 [C128 视频黑客](https://hackaday.com/2019/05/07/a-quite-obscure-c128-video-mode-hack/)中的【戴夫】。