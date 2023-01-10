# 您知道吗，Raspberry Pi 4 有更多的 SPI、I2C、UART 端口？

> 原文：<https://hackaday.com/2022/02/01/did-you-know-that-the-raspberry-pi-4-has-more-spi-i2c-uart-ports/>

我们已经习惯了树莓 Pi 电脑的 GPIO 可用功能多年来基本保持不变，这就是为什么它可能会有点不为人知:树莓 Pi 4 有[六个 SPI 控制器](https://blog.stabel.family/raspberry-pi-4-multiple-spis-and-the-device-tree/)、[六个 I2C 控制器和六个 UART](https://www.tomshardware.com/reviews/raspberry-pi-gpio-pinout,6122.html)——所有这些都在它的 40 引脚接头上。你不能一次利用所有这些，但通过将多达四个不同的连接导线连接到一个引脚，你可以为你的下一个机器人、自动化或养猫项目创造出一个非常强大的外设组合。

[这些外设的数据表](https://datasheets.raspberrypi.com/bcm2711/bcm2711-peripherals.pdf)很容易阅读，所有的寄存器映射都布局合理——即使您不打算自己处理寄存器映射，您首选的硬件支持库的维护人员也会更轻松！当然，这些外围设备也存在于计算模块 4 上。这可能会让人觉得这样泛滥的界面有些过分，但是，它让你实现了一些很酷的东西，否则是不可能的。

拥有多个 I2C 接口有助于[处理各种 I2C 特有的问题](https://hackaday.com/2016/07/19/what-could-go-wrong-i2c-edition/)，例如地址冲突、吞吐量问题以及支持不同最大速度的混合设备，这意味着你不再需要花哨的 mux 芯片来同时运行五个[低分辨率 Melexis 热感相机传感器](https://hackaday.com/2019/09/22/getting-the-heat-on-with-a-thermal-camera/)。(哦，I2C 时钟拉伸错误已经修复！)SPI 接口用于高带宽的设备，通过几个独立的 SPI 端口，你可以同时运行多个相对高分辨率的显示器，[无谢妮谢妮时钟风格。](https://hackaday.com/2021/04/20/no-nixie-nixie-clock/)

至于 UART，Raspberry Pi 的 1.5 UART 接口在机器人和家庭自动化应用中一直是个问题。有了一系列设备，如无线电接收器/发射器、[激光雷达](https://hackaday.com/2020/03/24/lidar-system-isnt-just-a-rangefinder-anymore/)和 UART 形式的弹性 RS485 多点接口，您不必再牺牲蓝牙或调试控制台来将一些花哨的传感器连接到机器人的大脑，这很好。您最多可以启用六个 UARTs。

## 如何使用这些接口？

启用这些接口似乎很简单，Raspberry Pi 论坛和其他地方的人们已经在为他们自己的努力进行测试。使用`config.txt`中的`dtoverlay`线可以启用所有三种接口。对于 SPI，[MaSt]博客[提供了一些有用的例子](https://blog.stabel.family/raspberry-pi-4-multiple-spis-and-the-device-tree/):

`# enabling SPI6 with two CS pins - one on GPIO16 and other on GPIO26
dtoverlay=spi6-2cs,cs0_pin=16,cs1_pin=26`

对于 I2C 和 UART，Raspberry Pi 论坛线程提供了一些例子。 [I2C 的例子](https://forums.raspberrypi.com/viewtopic.php?t=248439):

`# Enabling I2C3, with SDA on GPIO4 and SCL on GPIO5
dtoverlay=i2c3,pins_4_5`

[UART 示例](https://forums.raspberrypi.com/viewtopic.php?t=244827):

`# Enabling UART, with RTS and CTS pins (omit the 'ctsrts' part to disable them)
dtoverlay=uart3,ctsrts`

从这里开始，这些接口将按照您的预期出现，分别为`/dev/spi6`、`/dev/i2c-3`和`/dev/ttyAMA*`。(串行端口还没有别名，所以您将在现有端口的基础上再增加一个`/dev/ttyAMA`端口。)

我们很惊讶地了解到这些新的外设，也许你也一样？我们迫不及待地想知道你会用它们做什么。

主图由【Les Pounder】根据 Raspberry Pi 4 GPIO 引脚排列图[重新混合。](https://www.tomshardware.com/reviews/raspberry-pi-gpio-pinout,6122.html)