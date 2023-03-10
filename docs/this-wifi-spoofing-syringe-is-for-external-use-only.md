# 这款 WiFi 欺骗注射器仅供外用

> 原文：<https://hackaday.com/2019/08/08/this-wifi-spoofing-syringe-is-for-external-use-only/>

浏览一下他收集的作品，你会发现[埃尔·健太郎]喜欢将电子产品组装到有趣的外壳中，所以当他意识到 150 毫升的塑料注射器中有足够的空间来安装 ESP8266、电池和大量的 RGB LEDs 时，[“包注射器”是不可避免的结果](https://medium.com/@elkentaro/the-wifi-doctor-will-see-you-now-86aceb63673a)。

[![](img/443d95391a50bb05ed47a9f32ca8d65c.png)](https://hackaday.com/wp-content/uploads/2019/08/injector_detail.jpg) 理所当然的，这个装置的当前化身并没有*字面上的*注入数据包。但是[健太郎]实际上也没有打算做任何恶意的事情。注射器是一个有趣的恶作剧，让他带到他发现自己所在的各种黑客团体中，[就像我们在 DEF CON 26](https://hackaday.com/2018/08/21/all-the-badges-of-def-con-26-vol-2/) 上看到的他的 DEAUTH“bling”项链，所以任何实用功能都是锦上添花，而不是严格的要求。

最后，他为 Adafruit Feather HUZZAH 设计的代码使用 FakeBeaconESP8266 库按需推出虚拟网络。[这是我们在过去见过的一个小把戏](https://hackaday.com/2018/02/09/esp8266-broadcasts-memorial-wifi-spam/)，只要你没有发出任何特别令人不快的 SSIDs，这是一个相对无害的恶作剧。在这种情况下，[埃尔·健太郎]用宣布“无线医生在这里”的信标来强调他的彩色辉煌

但真正的问题是[健太郎]如何控制设备。所有东西都包含在注射器腔内，他使用 MPL3115A2 I2C 气压传感器来检测它何时被压缩。如果传感器读取的压力高于设定的基线，NeoPixel 环就会启动，假信标帧就会开始发出。放松活塞，代码会检测到压力下降并关闭一切。

如果这个版本引起了你的兴趣，[健太郎]在 WOPR 峰会上做了一个关于他的硬件设计哲学的精彩演讲，包括他如何设计和制造他的一些“最伟大的作品”；包括一款树莓派 Zero enclosure，遗憾的是，*并未*限于外用。