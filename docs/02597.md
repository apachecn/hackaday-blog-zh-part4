# Rad-Hard ARM 微控制器，因为陶瓷元件更冷

> 原文：<https://hackaday.com/2019/04/13/rad-hard-arm-microcontrollers-because-ceramic-components-are-just-cooler/>

如果你正在建造一个立方体卫星，很好，只要从货架上拿一个微控制器，你可能不需要担心辐射加固。如果你正在为国际空间站建造一个实验，只需使用任何旧的微控制器。深空？这有点难，你可能需要研究抗辐射和抗辐射的微控制器。微芯片刚刚宣布发布了两款符合这一规格的微型芯片，分别是耐辐射型和抗辐射型。

新设备是 [SAMV71Q21RT](https://www.microchip.com/SAMV71Q21RT) (耐辐射)和 [SAMRH71](https://www.microchip.com/SAMRH71) (rad-hard)，这两个 ARM Cortex-M7 芯片都运行在 300 MHz 左右，具有足够的 RAM 来做几乎任何你想用微控制器做的事情。外设包括 CAN-FD 和以太网 AVB、模拟前端控制器，以及对 I2C、SPI 和其它标准的支持。该芯片在太空中实现这一功能，采用陶瓷四方扁平封装，配有金色引线框架。这些是*漂亮的*设备。

微芯片有数量惊人的空间级硬硬件；这主要是因为他们几年前收购了 Atmel，是的，绝对有可能使用该芯片建造一个 rad-hard Arduino Mega 。

当然，真正需要超硬微控制器的人非常非常少；老实说，我希望只有一两个人会读到这篇文章，而且他们可能也收到了新闻稿。如果你曾经想建造一个去太空的东西，你想过度设计它的一切，你现在可以选择 ARM Cortex-M7。