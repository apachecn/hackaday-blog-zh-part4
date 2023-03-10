# 通过 USB 和 IIO 在任何 Linux 上使用 I C 传感器

> 原文：<https://hackaday.com/2022/12/01/using-i%c2%b2c-sensors-with-any-linux-via-usb-and-iio/>

连接 I2C 传感器通常与微控制器和单板机相关联，但是在任何运行 Linux 的系统上使用这样的 I2C 传感器都非常容易。毕竟，I2C(也就是 SMBus)是最有可能在你的电脑主板和外围设备上使用的接口之一。这意味着运行我们自己的设备，如众所周知的 BME280 温度、压力和湿度传感器，或 Si1145 光传感器，应该是小菜一碟。

在几年前的一篇博客文章中，【Peter Molnar】[详细解释了](https://petermolnar.net/article/linux-i2c-iio-collectd/)如何连接物理适配器以将 USB 连接的 I2C 接口添加到系统中。其核心是基于 ATtiny85 AVR 的 MCU，提供内置 USB 接口，运行 [I2C-Tiny-USB](https://github.com/harbaum/I2C-Tiny-USB/tree/master/digispark) 固件。

这里最重要的部分是 MCU 作为 i2c 设备出现在 Linux 内核中，需要加载`i2c-dev`驱动程序。此后，连接到适配器 MCU 的 I2C 总线的 I2C 设备可以通过 Linux 模块的 API 调用来使用，或者直接使用，或者通过现有的驱动程序来使用。[Peter]发现 BMP280 驱动程序带有 Debian Sid，例如。