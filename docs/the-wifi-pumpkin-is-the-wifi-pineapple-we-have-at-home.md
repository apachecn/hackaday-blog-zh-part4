# WiFi 南瓜就是我们家里的 WiFi 菠萝

> 原文：<https://hackaday.com/2022/10/27/the-wifi-pumpkin-is-the-wifi-pineapple-we-have-at-home/>

虽然网络曾经完全依赖于 5 类电缆、集线器和路由器，但现在我们大多数人都定期以无线方式进行连接。就像常规网络一样，无线网络也需要审计，于是[Brains933]决定为此开发一个工具，并给它起了个绰号叫 PumpkinPI_3。

这款手机的设计灵感来自于一款流行的商业测试工具 [WiFi 菠萝](https://hackaday.com/2018/10/25/portable-hacking-unit-combines-pi-with-wifi-pineapple/)。它运行 [WiFi 南瓜框架](https://github.com/zackhaikal/WiFi-Pumpkin)，允许用户在给定的无线网络上运行各种攻击。在其他功能中，它可以充当流氓接入点，运行中间人攻击，甚至在需要时欺骗 Windows 更新。

在这种情况下，[Brains933]抓了个树莓 Pi Zero W 来运行框架。它被塞在一个装有 Alfa Network AWUS036NHA 无线网卡的盒子里，因为它能够在监控模式下运行，这是一些更高级的工具所需的功能。它使用可充电的 LiPo 电池来携带，并且可以安装一个小屏幕来方便操作。

它应该被证明是在旅途中调查无线安全性的有用工具。或者，你可以变得更瘦，用 ESP32 进行攻击。

 [https://www.youtube.com/embed/kuff6GiFd7M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kuff6GiFd7M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

