# 无线引导程序让你不用更换 rom 芯片

> 原文：<https://hackaday.com/2022/04/05/wireless-bootloader-saves-you-from-swapping-rom-chips/>

将你的代码写入 Arduino、ESP32 或任何其他现代微控制器平台非常简单:通过 USB 连接设备，启动适当的软件平台，然后按下“程序”。但那些在 80 年代和 90 年代参加过嵌入式编程课程的人会记得一个更复杂的过程，包括在编程器、目标板和 UV 橡皮擦之间交换 EPROM 芯片。那个时代的老手可能甚至还记得如何用 nop 覆盖以前的程序，并在它后面放置新的代码，以节省自己去“空白芯片”箱的旅程。

如果你是一个复古计算机爱好者，想拥有现代工具的简单编程，但又想拥有独立 ROM 加载计算机的真实性，你可能想看看[Anders Nielsen]最新设计的用于 6502 单板计算机的无线引导加载程序[。这个项目的目标平台是一台漂亮的定制的基于 6502 的逆向计算机，安德斯在他的 Hackaday.io 页面](https://www.youtube.com/watch?v=NABU7gQDtcs)上详细记录了[。](https://hackaday.io/project/181897-abnielsencom-6502-sbc)

这里的基本思想是在目标系统上安装一个无线接收器，从连接到现代 PC 的发射器接收数据。当你点击“程序”时，目标代码被发送到 6502 机器，存储在 ram 中并被执行。无线链路由一对通过 SPI 通信的 nRF24L01 2.4 GHz 模块实现。由于[Anders]的 Mac Mini 没有 GPIO 端口，他将发射器连接到一个 Raspberry Pi，并通过网络链接对其进行控制。

在 6502 端，他用汇编语言编写了一个引导程序，它位碰撞 SPI 协议以与无线模块通信。包括一个简单的用户界面，允许用户控制程序的加载和运行。Github 上的所有代码和硬件文档[可供任何拥有类似 6502 系统的人使用。](https://github.com/AndersBNielsen/abn6502)

那些 nRF24L01s 是多功能的小东西:我们已经看到它们被用来传输任何东西，从 [MIDI 数据](https://hackaday.com/2022/02/17/sending-midi-wirelessly-with-the-nrf24l01/)到 [TCP/IP 链接](https://hackaday.com/2020/12/04/nerfnet-tunnels-tcp-ip-over-nrf24l01-radios/)，以及用于其他微控制器平台的[代码](https://hackaday.com/2014/03/07/using-an-nrf24l01-for-air-bootloading/)。

 [https://www.youtube.com/embed/NABU7gQDtcs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NABU7gQDtcs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

