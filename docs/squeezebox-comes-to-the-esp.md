# Squeezebox 来到 ESP

> 原文：<https://hackaday.com/2019/03/31/squeezebox-comes-to-the-esp/>

流媒体音乐现在可能来自云端的某个地方，进入你手机上的一个应用程序，并被发送到你拥有的几乎每一个娱乐设备的内置客户端，但曾几何时，最大的优势在于连接到你现有设置的专用流媒体设备。该市场的参与者之一是罗技(Logitech)及其 Squeezebox 系列产品，尽管最初的硬件可能已经停产，但由于罗技媒体服务器软件的免费性质和播放器中 slimproto 流协议的实现，它在专用用户群中仍然非常活跃。现在你可以在尽可能便宜的硬件上创建一个网络播放器，因为[Bgiraut]已经为 ESP32 和 ESP8266 开发了一个客户端。

软件[可以在 GitHub](https://github.com/bgiraut/SqueezeEsp32) 上找到，并附带警告，这是一个早期的概念验证，而不是一个完美的版本。它有两个播放选项，都需要一点额外的硬件，一个用于未压缩流的 I2S DAC 或一个用于压缩流的 VS1053 编解码器模块，但这两个都不需要很贵。

你可以从[它的下载页面](https://www.mysqueezebox.com/download)找到罗技媒体服务器，试试这个设备。与此同时，我们已经介绍了许多 Squeezebox 实现，包括在 [Raspberry Pi](https://hackaday.com/2013/04/13/squeezeberry-a-raspberri-pi-powered-squeezebox-appliance/) 和 [PogoPlug](https://hackaday.com/2013/01/11/building-an-inexpensive-squeezebox-client-replacement/) 上的实现。

感谢[joyoofdivisions]的提示。