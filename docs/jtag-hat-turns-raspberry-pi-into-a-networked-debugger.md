# JTAG 帽把树莓派变成了网络调试器

> 原文：<https://hackaday.com/2021/05/28/jtag-hat-turns-raspberry-pi-into-a-networked-debugger/>

在过去的一年左右，我们注意到在树莓 Pi 上使用 OpenOCD 的人数明显上升。对于探索各种微控制器和嵌入式设备来说，这是一个便宜而方便的解决方案，但并不总是最优雅的。为了改善这种情况，[【马修·梅兹】一直在制作一顶特制的 JTAG 帽子](https://github.com/blinkinlabs/jtag_hat)来稍微清理一下。

板载电平转换器允许您连接到 1.8 至 5 V 的 JTAG 和 SWD 接口，如果您从 Pi 本身为目标设备供电，甚至支持测量电压和电流。为了连接到您的目标，开放式硬件板具有非常适合跳线的“传统”引脚接头，以及专用的 10 引脚 Cortex 调试连接器。无论你是自己组装还是购买一个，如果你经常使用合适的芯片，它看起来肯定是一个值得拥有的工具。

[![](img/00e1ae5a8e26a1ad64b7cfca7933b0a0.png)](https://hackaday.com/wp-content/uploads/2021/05/jtagpi_detail.png) 除了硬件的设计文件，[Matthew]还提供了一些关于如何启动和运行软件方面的文档。从一张空白的 SD 卡开始，它引导您完成 Raspberry Pi 的初始设置，一直到安装和配置 OpenOCD 的补丁版本，该版本旨在支持 JTAG 帽。

如果你花更多的时间使用 8 位 AVR 芯片，不用担心。去年，我们报道了一个类似的项目，将每个人最喜欢的 Linux SBC [变成一个一体化的微控制器开发发电站](https://hackaday.com/2020/09/05/turning-the-raspberry-pi-into-a-mcu-programmer/)。