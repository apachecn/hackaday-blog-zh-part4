# ESPFLIX 将流媒体视频带入微控制器世界

> 原文：<https://hackaday.com/2020/08/11/espflix-brings-streaming-video-to-the-world-of-microcontrollers/>

如今，如果你有一台有点太旧的电视，不能直接访问流媒体服务，你有很多选择。Apple TV、Chromecast 和一系列 Android 盒子可以帮助您在屏幕上获取内容。然而，如果你真的停留在过去，ESPFLIX 可能就适合你。

![](img/ef0428be439fd50939070c6f5ac2f536.png)

Control of the system is achieved by an Apple TV remote.

是的，没错——这是一个运行在 ESP32 上的在线流媒体服务。[rossumur]通过仔细使用编解码器和一些有效的编码策略来实现这一壮举。视频是 MPEG1，分辨率只有 352×192。音频是通过 SBC 编解码器传输的，最初用于蓝牙设备。之所以选择它，是因为它的样本缓冲区很小，更容易在 ESP32 有限的 RAM 中解码。输出是通过 ESP32 本身生成的复合视频。

这些书本身由公共领域的内容组成，运行在 Amazon Web Services 实例上。由于 ESP32 上的 RAM 有限，没有太多的缓冲，所以[rossumur]正在为 AWS Cloudfront 实例提供资金，这应该可以在世界上大多数地方通过可靠的互联网连接使用 ESPFLIX。

我们以前已经看到过[rossumur]的工作，ESP_8_BIT 是这个项目功能的前奏。休息后的视频。

 [https://www.youtube.com/embed/oPL8Pj6ATrg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oPL8Pj6ATrg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

