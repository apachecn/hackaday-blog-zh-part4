# Arduino 供电的便携式函数发生器

> 原文：<https://hackaday.com/2018/09/03/arduino-powered-portable-function-generator/>

可以毫不夸张地说，我们中的许多人都承担了一两个项目，这些项目只不过是为我们的武器库添加一个新工具或一件新装备的一个不加掩饰的借口。对于一个满是闪烁的按钮装饰的测试设备的工作台，有一些东西要说，这就像是书呆子的珠光宝气。但是就像把你的名字写在钻石上一样，它会很快变得昂贵。

幸运的是，如今黑客掌握了足够的技术，DIY 测试设备可以帮你填满你的工作台，而不用掏空你的钱包。[【法兰斯基】创造了一个非常令人印象深刻的 Arduino 函数发生器，它在功能上丝毫不吝啬](https://www.instructables.com/id/Portable-Function-Generator-on-Arduino/)。凭借其全数字电路，能够产生高达 10MHz 的正弦波、三角波和方波，这是一款非常值得花 30 美元左右来打造自己版本的设备。

对于那些担心[Faransky]依赖 Arduino Nano 的 PWM 功能来产生波形的人，不要担心。该器件的核心是一个波形发生器 AD9833Arduino、旋转编码器和 16×2 LCD 提供了通过 SPI 控制它的接口。

不幸的是，AD9833 无法控制幅度，而幅度对函数发生器来说非常重要。所以[Faransky]使用一个 X9C104P 100KOhm 8 位数字电位计作为芯片输出端的分压器。

最后，他添加了一个 2000 毫安时 3.7V 锂离子电池和 TP4056 充电器，以及一个 DC-DC 升压转换器，为 Arduino 提供 5V 电压。不过，如果你想创建一个台式版本的设备，你可以删除这些组件有利于 5V 交流/DC 适配器。

我们已经看到了相当多的 DIY 函数生成器，[从极简构建](https://hackaday.com/2012/02/08/attiny25-based-function-generator-causes-a-wave/)到可以作为商业产品的硬件。我们甚至看到了一些[廉价的交钥匙函数发生器](https://hackaday.com/2018/05/17/review-fg-100-dds-function-generator/)，尽管通常的警告是物有所值。

 [https://www.youtube.com/embed/Xt2-HlCfXGs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Xt2-HlCfXGs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

