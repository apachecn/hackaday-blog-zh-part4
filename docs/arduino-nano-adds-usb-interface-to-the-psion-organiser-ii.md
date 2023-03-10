# Arduino Nano 为 Psion Organiser II 增加了 USB 接口

> 原文：<https://hackaday.com/2022/02/07/arduino-nano-adds-usb-interface-to-the-psion-organiser-ii/>

1984 年推出的 Psion 组织者系列定义了第一代电子组织者或 PDA(个人数字助理)。尽管这些设备已经有 30 多年的历史了，心灵感应组织者的场景依然生机勃勃:新的硬件和软件仍在由世界各地的爱好者开发。

![A USB interface connected to a Psion Organiser II](img/fdc6203325ddbd3c9e6f4af2f86d2d26.png)

The Organiser II, with its brand-new USB interface

其中一个狂热爱好者是[詹姆斯·斯坦利]，他为心灵感应组织者 II 设计并制作了一个 USB 接口。虽然提供 RS-232 端口的“CommsLink”模块在过去是可用的，但它变得很难找到，这启发了[James]基于 Arduino Nano 设计一个全新的模块。将它连接到 Psion 的数据总线是一件简单的事情，将八条数据线连接到 Nano 的 GPIO 端口。一组串联电阻用于防止总线争用，而无需添加粘合逻辑。

让软件工作起来有点困难:组织者的本地 OPL 编程语言不允许用户直接访问扩展端口的内存地址，因此[James]必须用 HD6303 机器码编写一个例程来执行读取，然后从 OPL 调用该例程，将结果显示在屏幕上。目前，该例程仅支持从 Arduino 读取数据，但将其扩展到双向接口应该也是可能的。

最后，[James]为 Arduino-USB 接口设计并 3D 打印了一个整洁的外壳，这使它看起来几乎与原始的 CommsLink 模块一样光滑。或许随着进一步的发展，这可能会变成另一种方式[将旧的 Psions 连接到互联网](https://hackaday.com/2019/08/03/raspberry-pi-helps-vintage-psion-find-its-voice/)。我们还推出了[一种新型的 Datapak 来增强组织者的记忆力](https://hackaday.com/2021/08/26/proto-pda-regains-its-memory-with-the-help-of-a-raspberry-pi-pico/)。

 [https://www.youtube.com/embed/enHQhHhHgmw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/enHQhHhHgmw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[萨拉托加杰里]！