# ESP8266 和 ESP32 WiFi 被黑！

> 原文：<https://hackaday.com/2019/09/05/esp8266-and-esp32-wifi-hacked/>

[Matheus Garbelini]刚刚推出了 [three (3！)流行的 ESP32/8266 系列芯片上的不同 WiFi 攻击](https://github.com/Matheus-Garbelini/esp32_esp8266_attacks)。他先通知了 Espressif(谢谢！)而且他们已经修补了大部分漏洞，但是如果你在关键环境下运行这些芯片上的软件，你最好尽快升级新的固件。

[![](img/71136347ba6d92da4e09d3c5a094b14b.png)](https://hackaday.com/wp-content/uploads/2019/09/esp8266_beacon_crash_scenario.png)

第一个缺陷是最简单的，只影响 ESP8266s。连接到接入点时，接入点会向 ESP8266 发送一个“AKM 套件计数”字段，其中包含可用于连接的身份验证方法的数量。因为 ESP 不对这个值进行边界检查，所以恶意的伪访问点可以在这里发送大量的数据，可能会溢出缓冲区，但肯定会使 ESP 崩溃。如果您可以向 ESP8266 发送虚假的信标帧或探测响应，就可以使其崩溃。

beacon frame crasher 最有趣的地方是它也可以在 ESP8266 上实现。崩溃了。这利用了 [ESP 的数据包注入模式](https://hackaday.com/2016/01/14/inject-packets-with-an-esp8266/)，我们之前已经介绍过。

第二个[漏洞](https://matheus-garbelini.github.io/home/post/esp32-esp8266-eap-crash/)和第三个[漏洞](https://matheus-garbelini.github.io/home/post/zero-pmk-installation/)利用了 ESP 库处理[可扩展认证协议](https://en.wikipedia.org/wiki/Extensible_Authentication_Protocol) (EAP)的方式中的漏洞，该协议主要用于企业和更高安全性的环境中。一种攻击使启用 EAP 的网络上的 ESP32 或 ESP8266 崩溃，但另一种攻击允许完全劫持加密会话。

这些 EAP 黑客更令人不安，这不仅仅是因为会话劫持比崩溃 DOS 场景更危险。ESP32 代码库已经针对它们打了补丁，但是旧的 ESP8266 SDK 还没有。所以现在，如果你在 EAP 上运行 ESP8266，你就容易受到攻击。我们不知道在 EAP 网络中有多少 ESP8266 设备，但我们真的希望看到 Espressif 弥补这个漏洞。

[Matheus]指出具有讽刺意味的是，如果你使用 WPA2，你实际上比没有打补丁和使用名义上更安全的 EAP 更安全。他还写道，如果您被困在一个 EAP 环境中，您至少应该对您的数据进行加密和签名，以防止窃听和/或重放攻击。

还是那句话，因为[Matheus]先通知了 Espressif，所以大部分的 bug 都已经修复了。它甚至渗透到了 Arduino-for-ESP 的下游，在那里它刚刚在几个小时前被开发成最新版本。是时候更新了。但是那些又老又硬的节点 MCU 建立了我们家里所有的东西？是时候完全重新编译了。

我们一直想知道何时能在野外看到第一次 ESP8266 攻击，那一天终于到来了。谢谢，马修！