# 需要逻辑分析仪吗？用你的对讲机。

> 原文：<https://hackaday.com/2022/03/02/need-a-logic-analyzer-use-your-pico/>

有许多硬件黑客问题，逻辑分析仪完全可以解决。无论你是想了解为什么 SPI LCD 屏幕无法初始化，你的 I2C 总线出了什么问题，还是想确定 UART 连接的速度，你都需要一个逻辑分析仪。人们一直在紧要关头使用 Pi Pico 作为逻辑分析器，现在[pico-coder] [分享了一个 sigrok 驱动程序](https://github.com/pico-coder/sigrok-pico)，它为 Pico 添加了对 Pulseview 等心爱工具的适当支持。

提供的规格令人印象深刻。与我们习以为常的 10 美元的“Saleae”克隆分析仪相比，这款设备拥有 21 个捕获速度高达 120 MHz 的数字通道，3 个高达 500 KHz 的 ADC 通道，以及基于硬件的触发器。上面链接的 GitHub 库存储了树外的驱动文件，[,但是提供了构建指令](https://github.com/pico-coder/sigrok-pico/blob/main/SigrokBuildNotes.md)和一个容易刷新的固件`uf2`。不过，鉴于我们在 sigrok 邮件列表上看到的提交者友好的态度，你很可能很快就会在 stock Pulseview 安装中看到这个驱动程序。然而，如果你急需逻辑分析仪，你应该遵循[贴心提供的快速入门指南](https://github.com/pico-coder/sigrok-pico/blob/main/GettingStarted.md)。

我们之前已经介绍过 Pulseview 与廉价易得的分析仪结合使用，如果您需要了解它们为业余爱好者提供的价值，那么[这是一款必看的产品。如果示波器是你所需要的，智能手机是你所拥有的，也许你会喜欢](https://hackaday.com/2017/07/29/everything-you-need-to-know-about-logic-probes/)[Pico](https://hackaday.com/2021/06/26/raspberry-pi-pico-oscilloscope/)的 Scoppy 固件。

我们感谢[mip]与我们分享这些！