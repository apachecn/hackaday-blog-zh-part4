# 为无线 GDB 行动的黑魔法添加 WiFi

> 原文：<https://hackaday.com/2020/06/04/adding-wifi-to-black-magic-for-wireless-gdb-action/>

[Thoquz]写信给我们，介绍了[Valmantas palika]的一个有趣的 GitHub 项目，该项目涉及将[黑魔法固件移植到 esp 8266](https://github.com/walmis/blackmagic-espidf)。对于那些不知道的人来说，[黑魔法探针](https://github.com/blacksphere/blackmagic/wiki)是固件，以及一系列[官方和第三方电路板](https://github.com/blacksphere/blackmagic/wiki/Debugger-Hardware)，旨在调试 Cortex-M 和 Cortex-A MCU 和 SOC。

通过这个 blackmagic-espidf 项目，用户可以使用任何具有至少 2 MB Flash 程序存储的 ESP8266 板，但如果禁用 OTA 更新，则应该可以使用 1 MB。将固件刷新到 ESP8266 板后，可以通过 TCP 端口 2022 和 UDP 2023 访问 GDB 服务器，并通过 TCP/23、UDP2323 或 ESP8266 上的物理 TX0/RX0 引脚提供串行端口。

要调试的目标板默认连接到 GPIO0 (SWDIO)和 GPIO2 (SWCLK ),用于串行线调试，尽管据说也支持 JTAG。如果设置正确，下一个应该能够弹出一个新远程 GDB 会话:

## [![gdb connection](img/f18fc014eceb4119c3249a0588ed400e.png)](https://github.com/walmis/blackmagic-espidf/blob/mastimg/gdb.gif)

如果你不想要 WiFi，你可以[买一个有线的，或者从你身边的任何 STM32 板](https://hackaday.com/2016/12/02/black-magic-probe-the-best-arm-jtag-debugger/)上滚动自己的。