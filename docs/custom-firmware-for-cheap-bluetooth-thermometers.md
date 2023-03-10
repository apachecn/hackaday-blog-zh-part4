# 廉价蓝牙温度计的定制固件

> 原文：<https://hackaday.com/2020/11/17/custom-firmware-for-cheap-bluetooth-thermometers/>

小米 LYWSD03MMC 温湿度传感器*便宜的离谱*。如果你一次买几个，你可以期待为这些方便的蓝牙低能耗环境传感器支付 5 美元一个。不幸的是，这种低廉的价格也带来了一点麻烦:你只能通过小米官方的智能手机应用程序或通过将其链接到该公司的智能家居中心之一来读取数据。或者至少，*用*是这样的。

在过去的一年里， [[Aaron Christophel]一直致力于为这些 Xiomi 传感器](https://github.com/atc1441/ATC_MiThermometer)开发替代固件，解锁数据，以便您可以按照自己认为合适的方式使用它。此外，它允许用户调整以前不可用的各种功能和设置。例如，您可以禁用通常显示在 LCD 上的小 ASCII 艺术笑脸，以指示房间的相对舒适度。

新固件通过 BLE 广告广播每分钟发布温度、湿度和电池电量。换句话说，这意味着客户端设备无需配对就可以从传感器读取数据。抓取这些数据非常简单，GitHub 页面包含了广播消息中每个字节的含义。避免直接连接不仅可以更容易地快速读取多个温度计的值，还可以让设备的 CR2032 电池使用更长时间。

但也许这个项目最令人印象深刻的部分是如何安装定制固件。你不需要破解案件或焊接一个程序员。只需在支持网络蓝牙的电脑和浏览器组合(智能手机可能是最好的选择)上加载闪光器页面，指向你想要闪烁的温度计的 MAC 地址，然后点击按钮。[【亚伦】对于为他的固件项目开发用户友好的 OTA 安装程序](https://hackaday.com/2019/08/23/ota-flash-tool-makes-fitness-tracker-hacking-more-accessible/)并不陌生，但即使对他来说，这也令人印象深刻。

 [https://www.youtube.com/embed/NXKzFG61lNs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NXKzFG61lNs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

