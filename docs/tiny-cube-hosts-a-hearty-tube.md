# 小小的立方体承载着一根结实的管子

> 原文：<https://hackaday.com/2019/10/25/tiny-cube-hosts-a-hearty-tube/>

微小的 PCBAs 和 glowy VFD 电子管对黑客作家来说就像猫薄荷，所以当我们看到[仓鼠]的 [TubeCube 电子管段驱动程序](https://github.com/hamster/TubeCube)时，我们必须深入了解更多信息。我们不会把勒德埋在这里；在我们继续之前，让我们欣赏一段发光灯管的视频:

 <https://hackaday.com/wp-content/uploads/2019/10/hamster-many.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2019/10/hamster-many.mp4](https://hackaday.com/wp-content/uploads/2019/10/hamster-many.mp4)

TubeCube 的构建符合 MiniBadge badge addon 标准，主要用于托管 [SAINTCON](https://www.saintcon.org/) 会议徽章上的模块。单个 TubeCube 托管 VFD 管、提供 70 V 电源的硬件以及用于通信和控制的微控制器。每个 TubeCube 都被设计为通过 UART 接收 ASCII 字符以在它的显示器上显示，但是它们也可以被链接在一起以获得更多的刺激。我们不确定[仓鼠]如何能穿上上面视频中的野兽，但如果他能找到一种方法，他们就能一起工作。如果你有兴趣看死简单的 UART 通信方案，看看这个文件[。](https://github.com/hamster/TubeCube/blob/master/Software/TubeCube/TubeCube/main.c#L162)

![](img/88e02a4d9d3dc560e25d5a6b4bc82dfa.png)

我们认为高压电源也值得一提。对于我们中的软件或机械头脑来说，很容易陷入将开关电源视为只能使用一体化控制 IC 构建的神奇构造的思维。但是[仓鼠]的电源提醒我们，开关电源，即使是高压电源，也没有那么复杂。他的设计(他说是抄袭了 Adafruit 可爱的冰管钟)本质上是由标准的原型组成的。一个大的低压电容 C1 来产生将被提升的能量脉冲，必要的电感/高压电容 C2 最终达到目标电压，一个平滑电容 C3 使输出更好。它由微控制器控制，拨动 Q1 来控制流经 L1 的电流。副作用是通过控制 PWM 频率[仓鼠]可以改变管的亮度。

现在看起来这个库有一个原理图和源代码，这应该足以构建一个你自己的小型电子管驱动程序。如果你没有足够的 TubeCubes，休息之后还有一个视频(单个模块的)。

 <https://hackaday.com/wp-content/uploads/2019/10/hamster-single-1.mp4?_=2>

[https://hackaday.com/wp-content/uploads/2019/10/hamster-single-1.mp4](https://hackaday.com/wp-content/uploads/2019/10/hamster-single-1.mp4)