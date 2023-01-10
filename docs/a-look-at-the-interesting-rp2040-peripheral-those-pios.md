# 看看有趣的 RP2040 外设，那些 Pio

> 原文：<https://hackaday.com/2021/01/29/a-look-at-the-interesting-rp2040-peripheral-those-pios/>

Raspberry Pi Pico 是 Raspberry Pi 系列中的最新产品，它标志着他们与以前支持 Linux 的小型主板的区别。小小的微控制器板肯定会在 Pi Foundation 的核心市场上表现出色，但它的 RP2040 芯片必须有一些特殊的商业组件，以避免成为 ARM 微控制器的另一个版本，ARM 微控制器碰巧更贵一些，并且来自芯片领域未经验证的制造商。也许这种特殊的东西来自它的机载可编程 IO perhipherals，或 PIOs。[【CNX 软件】对它们进行了深入的研究](https://www.cnx-software.com/2021/01/27/a-closer-look-at-raspberry-pi-rp2040-programmable-ios-pio/)，这是一篇有趣的阅读。

Pio 是一组状态机，它们有自己简单的汇编语言来执行简单的重复性 I/O 任务，而不需要主处理器内核的关注。如何配置取决于程序员的想象力，但建议的例子是额外的 I2C 或 SPI 总线，或视频接口。我们预计黑客社区会用意想不到的应用程序将他们推向极端，就像 ESP32 的 I2S 外设一样。本文介绍了汇编语言，然后用汇编语言、C/C++和 Python 给出了简单的例子。如果你有一个树莓皮皮可，那么你肯定会想和皮奥一起玩，我们期待看到你想出的东西。

[你可以在这里](https://hackaday.com/2021/01/20/raspberry-pi-enters-microcontroller-game-with-4-pico/)阅读 Hackaday 对 Pico 的评论。