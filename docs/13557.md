# 使用这个裸机编程环境释放您的 Pi

> 原文：<https://hackaday.com/2022/05/08/free-your-pi-with-this-bare-metal-programming-environment/>

不久前,[Rene Strange]用一个基于 poly synth 的甜美的 Raspberry Pi 软件美化了这些页面，并诱人地提到它是一个裸机应用程序。所以现在，我们来看看 [circle，它所基于的裸机编程环境](https://github.com/rsta2/circle)。该平台由一大组 C++类组成，用于访问硬件以及在协作多任务、多核环境中执行任务，如任务创建和调度。支持从版本 2 开始的所有 Raspberry Pi 板(不包括 Pico！)在 32 位和 64 位版本中，环境都相当完整。为 USB、网络、FatFS 以及更普通的任务(如处理中断)提供了类。在这些类的顶部有一堆特定于应用程序的库，包括显示接口、使用各种框架的 GUI 等功能，以及一些更深奥的应用程序，如与 Pico 接口，甚至将系统日志发送到远程 web 浏览器！

然而，类和库本身并不总是有用的，这就是 42 个(是的，我们知道)代码示例非常有用的地方。他们提供了一些有趣的示例应用程序，如在显示器上绘制 Mandelbrot 分形，以及一些我们必须处理的更普通的任务，如让讨厌的 DMA 控制器与 SPI 硬件配合良好。总而言之，这看起来是一套很棒的工具，可以充分利用一些相当强大的硬件，用于下一个需要大量资源的嵌入式项目，但不是所有不必要的操作系统东西。

也许不像 circle 那么完整，但这些年来我们已经看到了相当多的 Raspberry Pi 裸机项目，比如基于 PiZero 的 [Nerdsynth](https://hackaday.com/2016/01/17/pi-zero-video-card-via-bare-metal-programming/) ，以及 starfox 的这个[简洁的裸机汇编语言克隆。](https://hackaday.com/2014/06/23/programming-pi-games-with-bare-metal-assembly/)

谢谢[Ruhan]的提示！

Header:雅利安帕蒂达尔，[CC BY 4.0](https://commons.wikimedia.org/wiki/File:Metal_Work_Sparks.jpg)/埃文-阿莫斯，[公共领域。](https://commons.wikimedia.org/wiki/File:Raspberry-Pi-2-Bare-BR.jpg)