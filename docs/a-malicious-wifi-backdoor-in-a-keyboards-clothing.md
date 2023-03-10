# 一个藏在键盘衣服里的恶意 WiFi 后门

> 原文：<https://hackaday.com/2019/02/12/a-malicious-wifi-backdoor-in-a-keyboards-clothing/>

几年前，USB 橡皮鸭突然出现，并发明了一种新的攻击载体——击键注入。恶意 USB 设备将自己作为目标系统的键盘，以每分钟高达 1000 个单词的速度脱口而出击键。该设备通常用于打开网络钓鱼网站或输入命令以窃取受害者的数据。现在，事情又上了一个台阶，esploitv 2——一种支持 WiFi 的相同概念。

该设备运行在 Cactus WHID 平台上，因此得名于它采用的 ESP12 WiFi 微控制器，以及用于 USB HID 设备仿真的 Atmega 32u4。凭借其无线连接，有抱负的黑客不再需要依赖预先准备好的程序。各种攻击可以存储在 ESP12 宽敞的 4 兆闪存中，如果你觉得大胆，甚至有可能现场输入你的攻击。

这表明，我们对外国 USB 设备的信任是我们未来失败的潜在原因。 [BadUSB 是另一个很好的例子](https://hackaday.com/2014/10/05/badusb-means-were-all-screwed/)，而[如果你坚持使用不可信的端口，USB 包装器是一个很好的充电方式](https://hackaday.com/2014/03/21/dont-just-go-sticking-that-anywhere-protect-the-precious-with-a-usb-wrapper/)。