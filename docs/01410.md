# 新零件日:25 美分 USB 微控制器(带工具链！)

> 原文：<https://hackaday.com/2018/11/30/new-part-day-the-twenty-five-cent-usb-microcontroller-with-a-toolchain/>

去年，江苏宇恒股份有限公司推出了一款新的微控制器。[ch 554](http://www.wch.cn/products/CH554.html)是一款微控制器，带有一个 24 MHz 时钟的 E8051 内核、稍大于 1 kB 的 RAM 以及稍大于 14 kB 的代码和数据闪存。简而言之，它没有什么太壮观的，但它用外设弥补了这一点。它有 SPI、ADC 和 PWM、UARTs，甚至还有几个容性触摸通道。它也是一个 USB 设备，该系列中的一些芯片可以充当 USB 主机。你可以通过通常的零售商花 25 美分买到这种芯片。

通常，这不是什么大新闻。8051 是这个星球上被复制最多的微控制器，每年大概生产数十亿个。便宜的零件只有在你时间空闲的情况下才便宜；您通常会花很长时间来消化数据手册，并启动和运行工具链。这就是这个芯片有点不一样的地方。有多种努力将开源工具链引入该芯片。他们在 Windows 和 Linux 上做这个。有人真的很在乎这个芯片。

目前这款芯片的 SDK 最佳选择[来自 Blinkinlabs](https://github.com/Blinkinlabs/ch554_sdcc/) ，CH554 SDK 的一个端口从 Keil 到 SDCC。这款芯片使用开源工具链，有真实的工作代码示例。当然，它可能只是闪烁的 LED，但它是存在的。如果你能让 LED 闪烁，你就能从那里做任何事情。用“官方”的 [WCHISPTool](http://www.wch.cn/download/WCHISPTool_Setup_exe.html) (Windows)或 [LibreCH551](https://github.com/rgwan/librech551) (命令行)通过 USB 对芯片进行编程。最终结果是一个完全开源的工具链，可以编程并上传一个十六进制文件到一个便宜的芯片上。

CH554 系列中有更多的芯片，从 SOP-16 封装的 CH551 到 LQFP48 封装的 CH559，随着芯片变大，可以提供更多的功能。这是一个有趣的芯片，有些以某种方式实现了 USB 集线器，对于一些低级 USB 黑客来说可能是一个非常酷的芯片。