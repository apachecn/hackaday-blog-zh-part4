# ESP8266 制造无线读卡器

> 原文：<https://hackaday.com/2020/07/25/esp8266-makes-a-wireless-card-reader/>

你可以找到商业 u 盘，也可以通过 WiFi 连接。但是[中微子] [利用一个与读卡器相连的 ESP8266 制造了自己的](https://www.youtube.com/watch?v=s3kLNe_z6iI)。这一切都始于将接头焊接到 SD 卡适配器的老技巧。USB 口还在，只是为了电源。一个 3.3 V 稳压器和一个 ESP12E 板完善了硬件。

当然，诀窍在于软件。从几个例子开始，他最终提供了一个 FTP 服务器，您可以连接到该服务器并使用该协议发送或接收文件。

听起来似乎是一些设计上的妥协导致了这个设备有点慢，尽管它看起来很有用。[中微子]想换成 ESP32，并做一些其他的改变，以获得更好的速度。

当然，你可以去买一个 SanDisk Connect Wireless 或者类似的产品，但是这有什么意思呢？此外，能够将 SD 卡连接到您的项目为数据记录、配置等打开了许多可能性。

老实说，我们对大多数商业无线内存产品的结果都相对较差，包括古老的 [FlashAir](https://hackaday.com/2015/08/15/hacking-an-sd-slot-for-wifi/) ，所以拥有一个你可以完全控制的设备是有吸引力的。如果你有一个 SD 卡连接到一个项目，你可以做的一件事是[播放一些曲子](https://hackaday.com/2014/12/25/8-bit-chip-rocks-16-bit-44-1khz-tunes/)。

 [https://www.youtube.com/embed/s3kLNe_z6iI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/s3kLNe_z6iI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

