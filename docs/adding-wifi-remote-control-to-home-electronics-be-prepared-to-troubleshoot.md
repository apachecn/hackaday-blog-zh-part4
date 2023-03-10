# 给家用电子产品加 WiFi 遥控器？准备排除故障

> 原文：<https://hackaday.com/2022/01/19/adding-wifi-remote-control-to-home-electronics-be-prepared-to-troubleshoot/>

[Alex]最近为 Marantz 音频放大器[提供了通过 WiFi 远程控制的能力，方法是将 ESP32 板连接到一个方便的端口](https://smallhacks.wordpress.com/2021/12/20/adding-web-based-remote-control-to-my-marantz-amplifier/)，但该过程凸显了与现有硬件的连接经常会遇到一些不可预见的小问题，如果不解决这些问题，项目就会失败。

该项目的核心是使用 ESP32 和 [ESPAsyncWebServer](https://github.com/me-no-dev/ESPAsyncWebServer) 项目来创建一个可以通过 WiFi 访问的便捷网络界面。然后，为了实际控制放大器，[Alex]通过观察该单元的远程端口解码基于红外的远程信号，这些端口旨在作为红外信号到其他 Marantz 单元的传递和中继器。可以利用这种功能；[通过向远程输入端口发送正确的信号，该装置可由 ESP32](https://smallhacks.wordpress.com/2021/07/07/controlling-marantz-amplifier-using-arduino-via-remote-socket/) 控制。由于几乎任何 WiFi 设备都可以访问 ESP32，因此[Alex]可以自由控制他的放大器，比红外遥控器更灵活。

听起来相当简单，但像往常一样，当连接到现有的电子产品时，会有一些小故障。首先，高且不一致的延迟(从 10 ms 到 100 ms)使得控制放大器有时令人沮丧，但这可以通过禁用 WiFi 接口的省电功能来解决。另一个问题是，通过将 GPIO 引脚连接到放大器的远程输入端口来发送信号是可行的，但副作用是导致放大器不再监听 IR 遥控器。显然，从远程端口流向 ESP32 的 GPIO 引脚的电流是罪魁祸首，因为在两者之间添加一个二极管解决了这个问题。

GitHub 库保存了设计文件和代码。这种项目可能相当复杂，因为现有的硬件并不总是运行良好，而且像现代 ESP32 这样有用的主板也不总是可用。[在过去，给老式音频设备增加无线接口需要蚀刻电路板和更多的零件](https://hackaday.com/2011/08/19/adding-wireless-controls-to-vintage-stereo-equipment/)。