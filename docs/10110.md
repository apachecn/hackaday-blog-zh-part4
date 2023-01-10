# 使用 ESP32 进行 WiFi 渗透测试

> 原文：<https://hackaday.com/2021/05/27/wifi-penetration-testing-with-an-esp32/>

WiFi 是我们大多数人生活中离不开的技术之一。不幸的是，在底层的 802.11 标准中有几个潜在的漏洞可以被利用。为了证明这有多简单，[ risinek ]开发了 [ESP32 Wi-Fi 渗透工具](https://github.com/risinek/esp32-wifi-penetration-tool)，它运行在廉价的开发板上，可以执行取消认证和拒绝服务攻击，并捕获握手和 PMKIDs。

该项目的主要挑战是在使用 ESP-IDF 开发框架的同时实施这些攻击。ESP-IDF 的封闭源代码 WiFi 库会阻止特定的任意帧，如[去认证](https://hackaday.com/2017/08/13/wifi-deauthentication-vs-wifi-jamming-what-is-the-difference/)帧。为了解决这个问题[ risinek ]使用了两种不同的方法。第一种是在编译时绕过阻塞函数的声明，这是从 esp32-deauther 项目借用来的。第二种方法不需要对 ESP-IDF 进行任何修改。它的工作原理是创建一个与目标接入点相同的恶意接入点(AP ),每当其中一个设备试图连接到它而不是真正的 AP 时，它就会发送一个取消身份验证帧。

WPA/WPA2 握手是通过被动侦听连接到目标网络的设备，或运行 deauth 攻击，然后侦听设备何时重新连接来捕获的。通过分析 WPA 握手的第一条消息，从启用了漫游功能的 AP 捕获 PMKIDs。ESP32 Wi-Fi 渗透工具还会将捕获的数据格式化为 PCAP 和 HCCAPX 文件，以备 Wireshark 和 Hashcat 使用。为了管理该工具，它创建了一个管理访问点，在这里选择目标和攻击类型，并可以下载结果数据。将 ESP32 与电池配对，一切都可以在旅途中完成。该项目是[ risinek ]硕士论文的一部分，完整的[学术文章](http://excel.fit.vutbr.cz/submissions/2021/048/48.pdf)是一篇教育读物。

这些攻击都不是新的，它们已经在 Raspberry Pis 上运行了一段时间。 [Pwnagotchi](https://hackaday.com/2019/10/16/a-tamagotchi-for-wifi-cracking/) 是一个流行的例子，它可以在 Pi Zero 上运行。

 [https://www.youtube.com/embed/9I3BxRu86GE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9I3BxRu86GE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

