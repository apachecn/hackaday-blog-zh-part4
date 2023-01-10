# 使用 RGBeacon 为物联网设备轻松配置网络

> 原文：<https://hackaday.com/2022/05/11/easy-network-config-for-iot-devices-with-rgbeacon/>

当您将硬件连接到网络时，有时很难弄清楚设备的最终 IP 地址。[Bas Pijls]经常在课堂上看到这种问题，并着手为小型设备创建一种简单的方法来交流其 IP 地址和其他数据。

[Bas]特别想要一种不在硬件上增加显示屏的方法，因为这会给简单的物联网设备增加很多复杂性和费用。相反，RGBeacon 应运而生，其中微控制器借助单个 RGB WS2812B LED 闪烁出网络信息。

事实上，RGB LED 的所有三种颜色都用于通过网络摄像头向计算机发送信息。红色通道闪烁出时钟信号，绿色通道表示一个字节的开始，蓝色通道闪烁表示位为高电平。通过一点信号处理，在网络浏览器中运行 Javascript 应用程序的计算机可以通过网络摄像头接收来自闪烁 led 的微控制器的信息。

这是一个巧妙的技巧，应该会使在[Bas]的类中设置设备变得容易得多。它也不必局限于网络信息；这些代码可以被重新利用，让微控制器也能闪现其他信息。这与老式的 [Timex Datalink](https://hackaday.com/2022/03/26/arduino-keeps-your-classic-timex-datalink-in-sync/) 手表没有什么不同，它使用监视器闪光灯进行通信！