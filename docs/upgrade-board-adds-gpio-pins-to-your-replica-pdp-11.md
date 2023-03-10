# 升级板将 GPIO 引脚添加到您的副本 PDP-11

> 原文：<https://hackaday.com/2021/09/01/upgrade-board-adds-gpio-pins-to-your-replica-pdp-11/>

像许多 Hackaday 读者一样，[Steven Stallion]对[Oscar 维穆伦]创造的 PDP-11 复制品已经有一段时间了，今年夏天他终于有机会自己制作一个。虽然大多数用户可能满足于看着基于 Raspberry Pi 的仿复古电脑在货架上闪现，但他想探索将这种机器投入更多实际用途。最终结果是 PiDP-11 I/O 扩展器，这是一个让现代小型机与周围世界互动的附件。

基于微芯片 MCP23016 的扩展板是在与[Oscar]本人讨论后开发的，它非常适合 PiDP-11 PCB，并且[Steven]已确保他的安装指南与副本的文档相吻合。Pi 的 I2C 总线实际上是在原来的 PCB 上断开的，所以你只需要焊接一个接头，并在安装扩展器的地方连接一些跳线。你还需要拉 5 V 电压，安装指南中有一些关于方便连接点的提示。

[![](img/f254c14466fa23f6dfebe45ddd7aa878.png)](https://hackaday.com/wp-content/uploads/2021/08/pdpgpio_detail.jpg)

The installed PiDP-11 I/O Expander

每个扩展板都有 16 个 GPIO 引脚，可以通过 I2C 访问，包括对中断的支持，中断已经连接到 Raspberry Pi 上的 GPIO 19。[Steven]指出，如果您需要更多空闲引脚，您应该能够堆叠他的扩展器的倍数，尽管可能有必要摆弄一下上拉电阻和 I2C 地址。

用于扩展器的 PCB 已经在双条款 BSD 许可下发布，所以你可以自由地创建你自己的副本。但是如果你想节省一些时间，[[Steven]正在 Tindie](https://www.tindie.com/products/sstallion/pidp-11-io-expander-kit/)上提供组装板。

自从[【Oscar】在 2015 年 hack aday super conc](https://hackaday.com/2015/12/05/experiences-in-developing-an-electronics-kit/)上第一次取笑它，我们就被他神奇的 PDP-11 复制品迷住了。我们总是很高兴看到有人拿起了这些神奇的工具，尤其是[想出了一个以意想不到的方式扩展它的方法](https://hackaday.com/2019/03/31/a-weather-station-fit-for-a-pdp-11/)。