# 将 ESP8266 从开发板中解放出来

> 原文：<https://hackaday.com/2021/11/03/liberating-the-esp8266-from-its-development-board/>

虽然 ESP32 显然是一款出色的硬件，但我们认为您会同意，ESP8266 实在太有用了，在任何给定的时间都不会有一打左右的零件闲置。价格低廉、易于使用，并且功能足够将您的项目带入奇妙的物联网世界。但是如果你真的想充分利用它，你最终将不得不跳过开发板，开始使用裸模块本身。

这可能是一个可怕的转变，但幸运的是，[Ray]收集了一些笔记，这些笔记应该会对任何希望在自己的定制 PCB 中使用 ESP-12F 这样的模块的人有所帮助。从确保高耗电模块获得足够电量的不同技巧，到帮助减少电路设计所需辅助器件的成本削减措施，无论是新手还是老手，都值得一读。

[![](img/605d1bca96aaf5984bf8666e2dc0e1e3.png)](https://hackaday.com/wp-content/uploads/2021/10/esptips_detail.png)

An auto-reset circuit with the CH340C

例如，[Ray]谈到了使用臭名昭著的 GPIO10 引脚。此引脚位于 ESP8266 模块的背面，在许多开发板上，它甚至没有连接。这是因为它的内部连接到 ESP8266 的 SPI 闪存芯片，如果不小心使用它会导致问题。但正如博文中解释的那样，只要你[确保将闪存模式设置为“双 IO”(DIO)](https://hackaday.com/2017/10/01/trouble-flashing-your-esp8266-meet-dio-and-qio/)，那么 GPIO10 就可以像任何其他空闲引脚一样使用。

我们也很喜欢[Ray]在最后分享的技巧，让你的电路板更容易编程。当然，您可以在电路板上留下一个未填充的接头，或者摆弄一些弹簧针设置，但他的边缘连接器方法非常聪明。只需将编程器放在初始刻录上，然后就可以通过无线方式更新了。

不可否认，用 ESP8266 开发板组装东西是多么容易，[但是我们已经报道了太多令人难以置信的项目](https://hackaday.com/2020/01/08/an-esp8266-environmental-monitor-in-your-usb-port/)，这些项目[利用了裸模块的微小尺寸](https://hackaday.com/2021/08/13/hacked-ikea-air-quality-sensor-gets-custom-pcb/)，如果你不去掉中间人，你最终会被遗漏。