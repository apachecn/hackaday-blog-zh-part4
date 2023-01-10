# 隔离示波器设计流程展示了如何做到这一点

> 原文：<https://hackaday.com/2021/11/18/isolated-oscilloscope-design-process-shows-how-its-done/>

[Bart Schroder]正忙于设计高压变速电机驱动器，并哀叹标准示波器无法显示开关晶体管周围的波形。这是因为这种电机的三相特性是由三个电流波形驱动的，这三个电流波形彼此异相 120 度，其中电流在每对绕组抽头之间流动，而没有参考接地的公共概念。然而，你工作台上的平均示波器肯定是以地为基准的，所以可视化这样的波形有点麻烦。还有一个事实是，电机运行在数百伏的电压下，用你珍贵的台式仪器来探测这一点，至少可以说有点伤脑筋。这个问题的解决方案是显而易见的，建立自己的隔离高压示波器，这里是 [Cleverscope CS448 开发之旅](https://www.cleverscope.com/files/The%20Cleverscope%20CS448%20Development%20Journey.pdf)供您观赏。

作用域本身是规范的，没有什么特别的，是隔离的通道使它变得特别。然而，它也有一些细微之处，如额外的 8 个 100 Mbps 数字输入和一个方便的 65 MHz 信号发生器。此外，现在还不要掏你的钱包，因为这是一种专业仪器，潜在用户群比普通仪器更小，所以这些设备相当昂贵。也就是说，我们最感兴趣的不是范围的存在，而是从问题到解决方案的过程。从[Bart]的旅程中可以学到很多东西，例如，前端 ADC 应该放在哪里？隔离边还是不隔离边？信号链的噪底决定了前者。

构建这种性质的多通道隔离仪器的真正问题在于从前端到公共后端的隔离。前端需要电源，因此通过设计精美的双线缠绕环形变压器进行前馈，这本身就是一个完整的故事。根据 [JESD204B](https://www.analog.com/media/en/technical-documentation/technical-articles/JESD204B-Survival-Guide.pdf) 的说法，数据通过一对 4.375 Gbps 压缩串行通道从 ADC 中吸出，使用定制的光纤链路模块。[Bart]说明了这一过程中的许多问题，只是为了说明构建这样的东西并不总是以您尝试的第一种方式工作。聪明(范围)的东西

还需要高电流探头吗？[我们已经为您介绍了](https://hackaday.com/2021/04/11/high-current-measurement-probe-for-oscilloscopes/)，既然我们谈到了隔离的话题，那么用一个[隔离 USB 串行板](https://hackaday.com/2014/04/27/galvanic-isolated-ftdi-saves-your-computer/)来保护您的笔记本电脑安全如何？