# VFD 壁式温度计

> 原文：<https://hackaday.com/2019/12/28/a-vfd-wall-thermometer/>

想用 VFD 电子管做点什么，但还不需要另一个时钟项目？在这种情况下，这款由[commanderkull] 设计的[壁挂式温湿度显示器可能正是你想要的。六个 IV-11 管，这种显示器是一种实用的方式来添加一些华丽的蓝绿色辉光到你的家或办公室。](https://imgur.com/a/VfKWqYv)

USB 供电的显示器使用 XL6009 和 XL7015 分别提供 IV-11 管所需的 24 V 和 1.8 V。这两者都可以用跳线断开，以便在不关闭整个设备的情况下关闭电子管，这在编程和调试显示器的 ATmega328P 微控制器时是一个有用的功能。每个管都通过 74HC595 移位寄存器和 UDN2981 驱动器连接到 ATmega。温度和湿度数据由异常常见的 DHT22 传感器提供，这或许并不奇怪。

如果你*正在*寻找用这些风格的电子管建造另一个时钟，[肯定有足够的现有技术让你开始](https://hackaday.com/2013/03/02/vfd-tube-clock-built-using-protoboard-and-free-formed-psu/)。我们还看到了[人造 VFD，你可以用在项目](https://hackaday.com/2018/03/26/its-a-nixie-its-a-vfd-no-its-a-custom-led-display-in-a-tube/)中，以防你不想处理电压要求和相对罕见的真实事物。