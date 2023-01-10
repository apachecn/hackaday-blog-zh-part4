# SPIDriver 向您展示了正在发生的事情

> 原文：<https://hackaday.com/2018/07/10/spidriver-shows-you-whats-going-on/>

当你调试两个通过 SPI 相互通信的电子设备时，会有很多问题发生。从头开始，信号可能是错误的:数据与时钟不同步，或者相位颠倒。除此之外，实际发送的数据需要对接收设备有意义。你发出的命令是正确的吗？

当什么都不工作的时候，你同时在这两个方面战斗，你可能需要不同的工具来调试每一个。示波器在物理层工作得很好，而总线盗版或更好的逻辑分析仪在数据层工作得更好，因为它可以为您进行解析。在我们看来，詹姆斯·鲍曼(James Bowman)的 SPI driver(SPI driver)就像是一个带着屏幕的巴士海盗——给了你在两条战线上战斗的机会。

SPIDriver 还有几个锦囊妙计:被测设备的电压和电流监控器，因此当你经历随机复位时，你甚至不必拿出万用表。我们问[詹姆斯]这些新增项目背后是否有一段悲伤的历史。他包括了这个 XKCD。

关于 SPIDriver 的一切都是开放的，所以你可以[检查硬件设计，浏览代码](https://github.com/jamesbowman/spidriver)，并根据你的口味修改所有的内容。说到公开赛，詹姆斯也是 [Gameduino](https://hackaday.com/2011/03/02/gameduino/) 和 [FPGA Forth soft-CPU](https://hackaday.com/2015/07/28/open-source-fpga-toolchain-builds-cpu/) 的幕后黑手。

它完全是众筹的，但几天后就要关闭了，所以如果你想要一个，就赶快上吧。

如果你想了解更多关于 SPI 调试的知识，我们已经[写了一个速成教程](https://hackaday.com/2016/07/01/what-could-go-wrong-spi/)。有了装备和技术，你至少还有一线生机。