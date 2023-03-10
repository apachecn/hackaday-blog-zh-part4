# 如何在 ESP32 上轻松设置安全的 OTA 固件更新

> 原文：<https://hackaday.com/2021/11/29/how-to-easily-set-up-secure-ota-firmware-updates-on-esp32/>

在电子物联网设备部署到世界上后，可能有必要对其进行重新编程或更新。但是，如果对设备的物理访问很麻烦或者不再可能，那就有问题了。

![](img/a2ae83751e2993a7a650f56856de4b1d.png)

OTA updates allow a device to download new firmware, install it, and reboot itself into the new version. Convenient? Yes. Secure? It definitely needs to be.

幸运的是，空中下载(OTA)固件更新是一件事情，允许嵌入式设备通过无线数据连接而不是物理硬件设备进行重新编程。安全性当然是一个问题，幸运的是 [[Refik]解释了如何建立一个基本框架，以便 ESP32 OTA 更新可以安全地发生](https://www.lab4iot.com/2021/02/21/esp32-secure-firmware-update-over-the-air-ota/)，允许用户部署设备，并仍然可以放心地推送 OTA 更新。

[Refik]从使用 Ubuntu Linux 设置 web 服务器开始，使用来自 [Let's Encrypt](https://letsencrypt.org/) 的免费 SSL 证书设置 HTTPS，但是自签名 SSL 证书也是一个选项。一旦完成，就具备了支持以安全方式部署 OTA 更新的必要基础。再多一点配置，剩下的就靠物联网设备自己了。[Refik]解释了如何使用 [esp32FOTA 库](https://github.com/chrisjoyce911/esp32FOTA)进行设置，但我们也看到了[其他使 OTA 简单易用的方法](https://hackaday.com/2020/06/23/ota-esp32-gui-makes-updates-simple/)。

您可以在下面嵌入的视频中观看简单的安全 OTA 固件更新。有许多不同的部分在一起工作，所以[Refik]还为那些喜欢漫游的观众提供了第二个视频，以帮助他们弄清楚一切。休息之后，看他们两个。

 [https://www.youtube.com/embed/MDP93bWA0HE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MDP93bWA0HE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/5VhRwYo4NE0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5VhRwYo4NE0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

