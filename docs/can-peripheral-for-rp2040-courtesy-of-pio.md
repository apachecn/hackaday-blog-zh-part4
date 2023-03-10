# RP2040 的 CAN 外设，由 PIO 提供

> 原文：<https://hackaday.com/2022/07/09/can-peripheral-for-rp2040-courtesy-of-pio/>

[Kevin O'Connor]写信告诉我们他的项目，`can2040`–[为 RP2040 增加 CAN 支持。](https://github.com/KevinOConnor/can2040)RP2040 没有 can 外设，但是【凯文】为 RP 2040 的 PIO 引擎编写了代码，可以接收和发送 CAN 数据包。现在，通过使用这个公开可用的 can 驱动程序，我们都可以从他的工作中受益。这个库是用 C 语言编写的，所以它非常适合我们中的低级黑客，而且很有可能，围绕它制作一个 MicroPython 包装器并不难。

CAN 总线需要一个外设来正确处理消息，直到现在，人们一直使用外部芯片来实现这一目的。[Kevin]告诉我们，由于芯片短缺，这些芯片最近已经不可用，这使得这个项目更有价值。[文档内容丰富且易于访问，](https://github.com/KevinOConnor/can2040/blob/master/docs/Features.md)和【Kevin】详细介绍了如何最好地使用该驱动程序。有了这样的工具在手，您现在可以将您的 Pico 变成一个 can 修补工具包，或者连接一些 CAN 设备用于您自己的项目！

[Kevin]说这种代码已经被用于 Klipper，[一个支持](https://hackaday.com/2017/12/26/fast-3d-printing-with-raspberry-pi-but-not-how-you-think/) 3D 打印机和其他类似机器的框架。至于你自己的目的，你完全可以使用这样一个 can 工具来入侵你的汽车——这里有[一个汽车入侵文档的宝库，顺便提一下](https://hackaday.com/2017/05/14/car-security-experts-dump-all-their-research-and-vulnerabilities-online/)！得益于[PIO 引擎，](https://hackaday.com/2021/01/29/a-look-at-the-interesting-rp2040-peripheral-those-pios/)RP 2040 的多功能性似乎没有尽头——你甚至可以用[这种基于 PIO 的 DVI 代码来驱动 HDMI 监视器。](https://hackaday.com/2021/02/12/bitbanged-dvi-on-a-raspberry-pi-rp2040-microcontroller/)

标题图片[由 Florent.david.lille1，](https://commons.wikimedia.org/wiki/File:Le_bus_CAN_dans_l%27automobile.png) CC BY-SA 3.0