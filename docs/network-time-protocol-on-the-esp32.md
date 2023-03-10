# ESP32 上的网络时间协议

> 原文：<https://hackaday.com/2022/05/16/network-time-protocol-on-the-esp32/>

网络时间协议(NTP)是保持联网计算机同步到同一时间的最佳方式之一。它简单、轻便，不仅允许计算机一起维护一个时间标准，还允许一些计算机制造商在硬件成本上节省一些钱。Raspberry Pi 可能是最著名的低成本计算机的例子，它没有实时时钟(RTC)的额外费用。虽然 Pi 基本上自动设置 NTP，但 ESP32 等其他微控制器不会，但[可以配置它们使用这个时间标准，并做一些工作](https://bhave.sh/micropython-ntp/)。

对于这个项目，ESP32 的 MicroPython 实现是必需的。MicroPython 是一种在微控制器或其他嵌入式系统上运行 Python 代码的方式，没有 Python 通常需要的所有开销。幸运的是，NTP 库是内置的，所以一旦 MicroPython 在 ESP32 上运行，它几乎就像调用库一样简单。当然，你必须确保有互联网连接，然后抓住时间，同步到机器上，然后设置时区。

作为一个额外的练习，该项目的创建者[Bhavesh]建议尝试配置夏令时，尽管这可能是一个难以解决的问题。同时，在像这样的微控制器上安装时钟还有其他一些方法。一个 [RTC 模块](https://hackaday.com/2022/02/12/this-esp32-pico-wristwatch-has-plenty-of-potential/)是一个明显的选择，但是你也可以通过使用 GPS 模块获得[难以置信的精确时间。](https://hackaday.com/2022/01/20/ntp-server-gets-time-from-space/)