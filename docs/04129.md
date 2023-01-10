# 所有你想知道的关于红木微处理器和更多

> 原文：<https://hackaday.com/2019/09/09/everything-you-wanted-to-know-about-padauk-mcus-and-more/>

在这一点上，你需要住在月球黑暗面的岩石下，才能不听说这些神奇的 3 分微控制器。许多地方已经对它们进行了研究，但是很少有全面的综述，更不用说对这些红木 MCU 周围的整个生态系统的全面综述了。幸运的是，[Jay Carlson] [付出了很多努力](https://jaycarlson.net/2019/09/06/whats-up-with-these-3-cent-microcontrollers/)来收集你可能想知道的关于红木的一切。

最重要的一点是，这些 MCU 没有任何类型的通信外设。UARTs、I2C 和 SPI 都必须在软件中完成。由于功耗较高，它们不太适合低功耗或电池供电的应用。本质上，你会经常使用 GPIO 引脚。另一方面，它的多 CPU 上下文、FPPA 特性相当有趣，本文将详细介绍它。

至于开发工具，[Jay]对在线仿真(ICE)留下了深刻的印象，而不是在 MCU 上运行代码，因为这可以大大减少开发时间。这使得大多数 Padauk MCUs 的 OTP(一次可编程)属性甚至不如最初设想的那么重要。

然后是 MCU 的实际编程。Padauk 提供的微 C 编译器本质上实现了 C 语言的一个子集，用一些宏来代替像循环中的*这样的东西。起初，这似乎是一个奇怪的限制，直到你意识到这些 MCU 有 64 到 256 字节的 SRAM。那是字节，没有任何前缀。*

最后，[Jay]展示了几个测试项目，包括 NeoPixel SPI 适配器和自行车灯，这些都可以在 Github 上获得。WS2812b 项目是我们以前见过的，例如[来自【Anders Nielsen】](https://abnielsen.com/2019/04/24/driving-300-ws2812b-rgb-leds-with-a-3-cent-microcontroller-pms150c/)的这个项目(在文章图片中有特写)，它提供了这个系列的 MCU 的另一种形式。

看了[Jay]的文章有没有改变你对这些红木零件的看法？你以前用过这些 MCU 和 ICE 部件吗？欢迎在评论中留下你的想法。