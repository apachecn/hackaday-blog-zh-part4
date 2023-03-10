# Arduino 和 FPGA 的工作方式不同

> 原文：<https://hackaday.com/2021/03/21/arduino-and-fpga-done-differently/>

FPGA 专家[Max Maxfield]最近看了一家名为 Alorium 的公司的 XLR 8(发音为 accelerate)板。从表面上看，它看起来像另一个 Arduino UNO 克隆。但它不是 CPU，而是包含一个运行软核 AVR 处理器的英特尔 MAX10 FPGA。当然，这只是故事的一部分。如果该板只是一个使用 FPGA 的模拟 Arduino，那么实际应用起来就没什么意思了。然而，通过合并加速器模块或 XB，您可以将 FPGA 模块添加到软 CPU 中。[Max]展示了一个例子，您可以在下面的视频中看到，FPGA 模块比标准 Arduino 更容易控制伺服系统。还有一个版本看起来像 Arduino Nano，但可以更快地计时，也可以使用 XBs。

除了预构建的 XB，如果您熟悉使用 FPGAs，还有一个工作流可以构建自己的 XB。这些产品并不完全是新的，但我们喜欢(马克斯)对产品的理解。我们还欣赏了简单的代码示例，它准确地展示了如何转换程序以使用加速函数。

当然，这个想法不是新的或原创的。你可能会说 Arduino 的官方 FPGA 支持应该是这样的。帖子上的评论还谈到了之前几个从未获得太多关注的类似电路板，包括 [ZPUino](http://www.alvie.com/zpuino/) 。

几年前我们讨论过[类纳米板](https://hackaday.com/2018/04/30/tiny-arduino-fpga-sno/)。我们以前也见过使用 ZPUino 的[项目。](https://hackaday.com/2012/04/20/building-an-arduino-chiptunes-project-inside-an-fpga/)

 [https://www.youtube.com/embed/EkSMqOB0pL4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EkSMqOB0pL4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

