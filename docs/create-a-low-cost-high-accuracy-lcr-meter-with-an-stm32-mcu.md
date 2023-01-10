# 利用 STM32 MCU 创建低成本、高精度 LCR 计

> 原文：<https://hackaday.com/2019/07/20/create-a-low-cost-high-accuracy-lcr-meter-with-an-stm32-mcu/>

拥有一个好的 LCR 流量计是[Adil]想要在他的个人实验室中使用的东西，所以像任何优秀的大学生(和前 Hackaday 贡献者)一样，他最终建立了自己的。使用 [Nucleo-F446RE 板](https://www.st.com/en/evaluation-tools/nucleo-f446re.html)作为 MCU 侧，使用定制 PCB 作为实际测量侧，他创建了一个据说非常接近商用电表的电表，价格为 55 英镑。

贯穿设计背后的一些理论以及一些设计选择，然后展示最终的产品。此外，还解释了为何选择不使用标准分流器，而是使用[跨阻放大器](https://en.wikipedia.org/wiki/Transimpedance_amplifier) (TIA)。不幸的是，没有原理图或源代码，文本在某些方面有些不清楚，没有解释一些首字母缩写词，这使得在这个领域不活跃的人很难理解完整的设计。

我们希望[Adil]能够解决这些问题，并提供设计文件和源代码，因为它看起来确实是一个非常有趣的项目！