# MBed 上的 Arduino

> 原文：<https://hackaday.com/2019/08/30/arduino-on-mbed/>

有时候 Arduino 似乎无处不在。然而，随着新的物联网处理器过剩，在所有处理器上保持 Arduino 核心肯定是一项相当艰巨的任务。Arduino 的固件开发主管[Martino Facchin]在 Arduino 博客上写道，他们面临的问题是[支持来自北欧的两种新主板](https://blog.arduino.cc/2019/07/31/why-we-chose-to-build-the-arduino-nano-33-ble-core-on-mbed-os/)。

板，纳米 33 BLE 和纳米 33 BLE 的感觉是基于一个 ARM Cortex M4 中央处理器从北欧。当然，显而易见的答案是从头开始移植 Arduino 内核。然而，该团队不想只为几块电路板花费时间。他们考虑使用北欧库与硬件交互，但由于这是封闭的源代码，它并不真正符合 Arduino 的敏感性。然而，最终，他们采用了第三种方法，这可能是一种非常有趣的开发:他们将 Arduino 核心移植到 [Mbed OS](https://hackaday.com/2015/08/11/getting-started-with-arm-using-mbed/) 。甚至有一个在 Mbed 上加载[草图的例子，可从【Jan Jongboom】获得。](http://blog.janjongboom.com/2019/08/01/arduino-mbed.html)

一方面，这有两大好处:理论上，Arduino 现在可以在任何支持 Mbed 的东西上运行，这已经很多了。其次，尽管该系统保留了 Arduino 的简单性，但整个 Mbed 系统可供 Arduino 开发者使用，反之亦然。

另一方面，你可以争辩说，如果你有 Mbed，你真的不需要 Arduino。虽然对 Arduino 的简单性做了很多介绍，但它实际上是一个 C++程序，具有两个预定义的函数和一个 IDE，可以在没有您预期的那么多显式帮助的情况下构建您的代码。然而，支持 Arduino 的各种代码应该是令人感兴趣的，因为您可以毫不费力地从 Arduino 或 Mbed 程序中使用它。

这可能会让我们最喜欢的一些 Mbed labs 项目更受欢迎。如果你想看看我们的 Mbed 项目，你可以把它变成[一个信号发生器](https://hackaday.com/2015/09/15/how-to-build-a-pocket-sized-mbed-signal-generator/)。

谢谢[哈尔塔]的提示。