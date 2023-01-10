# I2C 和阿蒂尼一起到了极限

> 原文：<https://hackaday.com/2022/01/18/i2c-to-the-max-with-attiny/>

Arduino 是一个与现实世界交互的强大平台，但它不是没有限制的。即使对于 Arduino MEGA 来说，其中一个硬限制是微控制器可以用来与现实世界接口的引脚数量有限。但是，如果您希望在自己的项目中扩展该平台的应用范围，有几个选项可供选择。[Bill]的这个项目向我们展示了其中的一个选项，它使用 ATtiny85 通过 I2C 卸载一些 Arduino 的任务。

自 80 年代初以来，I2C 一直是微控制器使用最少的硬件相互通信的一种方式。所有需要做的就是连接微控制器的 I2C 引脚，并为每个引脚供电。这个项目使用 Arduino 作为控制器，任意数量的较小的 ATtiny85 微控制器作为目标。通过与较小的设备进行通信，Arduino 可以专注于更多处理器密集型任务，而将较简单的任务交给 ATtiny。它还极大地简化了可能分布在远处的项目的布线。[Bill]还为 ATtiny 定制了一个标准化的开发板，该开发板还可以兼作 Arduino 的屏蔽，使他可以轻松扩展和修改他的项目，而无需过多的额外焊接。

使用 I2C 可能不是最新颖的创新，但当受到 GPIO 或其他物理约束的限制时，让它易于使用无疑是一个有价值的工具。为此，[Bill]还提供了一个示例项目的代码，该项目简化了这些设备在软件端的设置。如果你正在寻找一些关于如何处理 I2C 的例子，看看[这个与 I2C](https://hackaday.com/2009/01/02/parts-i2c-digital-thermometer-tc74/) 通信的温度计或者[这个使用菊花链连接在一起的多个传感器的项目](https://hackaday.com/2018/05/23/automatic-i2c-address-allocation-for-daisy-chained-sensors/)。

 [https://www.youtube.com/embed/6BXPm6O2VaI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6BXPm6O2VaI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

