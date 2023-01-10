# ESP8266 转秘密 WiFi 探针请求嗅探器

> 原文：<https://hackaday.com/2020/09/20/esp8266-turned-secretive-wifi-probe-request-sniffer/>

当 Wi-Fi 设备打开时，它开始发出探测请求，试图找到一个熟悉的接入点。这些探测请求包含设备的 MAC 地址和它正在寻找的热点的 SSID，这可能被用来识别特定的设备和它去过的地方。在对这些探测请求进行实验后，[阿明·迈赫迪·曼苏里]创造了[open MAC，一个基于 ESP8266 的小型嗅探器，可以隐藏在任何地方](https://hackaday.io/project/174644-how-i-tracked-500-people-with-esp8266)。

该设备由一个 ESP-07S 模块、一个用于从 USB-C 连接器获取电源的调节器电路和一个用于电源循环的按钮组成。模块需要外部天线，可根据特定部署的尺寸或增益要求进行选择。[Amine]在当地图书馆测试了 OpenMAC(经过许可)，结合他自己的一些小 Wi-Fi 中继器来扩展网络的覆盖范围。所有记录的 MAC 地址都被记录到服务器上，这些数据可用于图书馆内部和周围的流量分析，甚至用于跟踪和定位特定设备。

这并不新鲜，是在零售场所收集信息的相对常见的技术，也可能被用于更邪恶的目的。较新版本的 iOS、Android 和 Windows 10 具有 MAC 地址随机化功能，这可以限制以这种方式跟踪设备的能力，但它并不总是被激活。

我们已经看到了许多利用探测请求的项目。 [FIND-LF 可以用来定位你家中的设备](https://hackaday.com/2016/12/25/track-wi-fi-devices-in-your-home/)， [Linger fools probe 通过重放先前记录的请求来请求嗅探器](https://hackaday.com/2017/04/29/linger-keeps-you-around-after-youve-gone/)。