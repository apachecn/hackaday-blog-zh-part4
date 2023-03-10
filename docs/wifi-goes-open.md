# WiFi 打开了

> 原文：<https://hackaday.com/2020/05/29/wifi-goes-open/>

对于大多数人来说，在一个项目中添加 WiFi 意味着抓住一个 ESP8266 或 ESP32 之类的东西。但是如果你在 FPGA 上开发自己的设计，那就意味着要增加一个包。如果你的目标是 Linux，OpenWifi 项目在 Verilog 中提供 Wifi 方面有一个很好的开端。在 [GitHub](https://github.com/open-sdr/openwifi) 上有许多开发板的例子和移植到你自己的目标的建议。你也可以在下面的视频中看到开发商之一的[Xianjun Jiao]演示整个事情。

该演示使用 Xilinx Zynq，因此 Linux 后端运行在 Arm 处理器上，与执行软件定义无线电的 FPGA 位于同一芯片上。我们要警告你，这个项目不适合胆小的人。如果你想理解代码，你必须钻研许多 WiFi 琐事。

不过好消息是许多高级功能都落在了通用 Linux 驱动程序上。除了用户空间控制程序，OpenWiFi 只提供驱动程序和 FPGA 配置。所有更高的细节都发生在可以与许多不同芯片组对话的 Linux WiFi 系统中。

该团队没有生产任何硬件，但使用了多个商用 FPGA 开发板。公平地说，如果你真的想在一个项目中添加 WiFi，并且你没有复制很多，有更简单的方法。但是，即使你的目标不是一个带 WiFi 的定制 ASIC，阅读 Verilog 并理解代码也能教会你很多关于 WiFi 内部的东西。

如果您需要更简单的东西来开始使用 FPGAs，请尝试我们的训练营。不觉得需要了解 WiFi 内部？也许吧。但是也许你也想知道你可能要防范哪种[攻击](https://hackaday.com/2017/02/03/jamming-wifi-by-jumping-on-the-ack/)。

 [https://www.youtube.com/embed/NW6-6N_EtrY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NW6-6N_EtrY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

