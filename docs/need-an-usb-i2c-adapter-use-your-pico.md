# 需要 USB I2C 适配器吗？用你的对讲机。

> 原文：<https://hackaday.com/2022/10/31/need-an-usb-i2c-adapter-use-your-pico/>

鉴于其丰富性和简单性，RP2040 无疑已成为 USB 外设构建的最爱——特别是用于电子实验的 USB 连接工具。今天，我们又看到了一个基于 Pico 的工具库的新成员——[(Renze Nicolai)开发的用于 RP2040](https://github.com/Nicolai-Electronics/rp2040-i2c-interface) 的 USB-I2C 适配器固件。这是基于 ATTiny 的 [I2C-Tiny-USB](https://github.com/harbaum/I2C-Tiny-USB) 项目的重新实现，并遵循相同的协议——因此，它与已经在 Linux 内核中存在多年的`i2c-tiny-usb`驱动程序兼容。只需拖动&放下`.uf2`，在您的 Linux 系统上运行一个脚本，您将从用户空间代码中获得一个可以使用的`/dev/i2c-X`设备，或者附加其他内核驱动程序。

该软件可与任何 RP2040 devboard 配合使用——只需将您的 I2C 设备连接到定义的引脚，您就可以在 Linux 工作站上的`i2cdetect`输出中看到它们。作为一个演示，[Renze]为其中一个 SSD 1306 128×64 OLED 编写了一个用户空间 Python 驱动程序，并为我们提供了一个命令行，让驱动程序接受一个`ffmpeg`命令的输出，捕捉您的主显示器的内容，在有机发光二极管上复制您的屏幕——与几个月前我们看到的[“HDMI”I2C 驱动的显示器](https://hackaday.com/2022/04/01/making-your-own-technically-hdmi-oled-monitor/)的方式类似。你可能需要的一切在 GitHub 页面上都可以找到，包括[使用说明和例子、](https://github.com/Nicolai-Electronics/rp2040-i2c-interface/tree/master/example)以及如果你想添加一个`udev`规则或改变 I2C 时钟频率时可以使用的几个脚本。

仅举几个例子，你可以使用 Pi Pico 作为 SWD 的工具， [JTAG](https://hackaday.com/2022/04/11/need-a-jtag-adapter-use-your-pico/) ， [CAN](https://hackaday.com/2022/07/09/can-peripheral-for-rp2040-courtesy-of-pio/) ，[具有数字和模拟通道的逻辑分析器](https://hackaday.com/2022/03/02/need-a-logic-analyzer-use-your-pico/)，甚至作为[一个小型的 EMP 驱动芯片毛刺工具。现在无处不在的 3 美元 Pi 微型主板似乎是怀念过去的黑客工具的有力竞争者，例如传说中的 BusPirate。](https://hackaday.com/2022/01/15/glitch-your-way-to-reverse-engineering-glory-with-the-picoemp/)

 [https://www.youtube.com/embed/PMtY5OU9V3Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PMtY5OU9V3Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

