# 物联网的 HTTPS

> 原文：<https://hackaday.com/2018/10/21/https-for-the-internet-of-things/>

每天，我们都在通过互联网连接越来越多的设备。一个家庭不再只有一台联网的电脑——有智能手机、平板电脑、暖通空调系统、插销——你能想到的，它都已经联网了。随着物联网的激增，安全性成为这一领域的一个问题已经变得非常明显。[[Andreas Spiess]一直致力于解决这个问题，他将 HTTPS 带到了 ESP8266 和 ESP32。](https://www.youtube.com/watch?v=Wm1xKj4bKsY&feature=youtu.be)

作为 IOT 设备最受欢迎的平台，在提高安全性时从 ESP 设备开始是有意义的。在他的视频中，[Andreas]从头开始，讲述了 SSL 的基础知识，然后扩展到如何将这些嵌入式系统与安全云服务结合使用，以及这样做的内存要求。[【Andreas】已经在 GitHub](https://github.com/SensorsIot/HTTPS-for-Makers) 上发布了代码，因此它可以很容易地包含在您自己的项目中。

显然，实现增强的安全性不是免费的；在处理能力、内存和代码复杂性方面是有代价的。然而，如果 IOT 设备要在更广泛的社会中得到信任，这些步骤是至关重要的。一个故障的发微博的咖啡壶是一回事，但是被锁在门外完全是另一回事。

[我们以前也看到过针对 ESP8266 安全性的其他攻击](https://hackaday.com/2017/06/20/practical-iot-cryptography-on-the-espressif-esp8266/)。随着这一领域的不断扩展，我们期待着更多的机会。

【感谢 Baldpower 的提示！]