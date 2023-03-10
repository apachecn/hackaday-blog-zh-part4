# 涡轮斯巴鲁获得 DIY 量表

> 原文：<https://hackaday.com/2019/05/29/turbo-subaru-gets-diy-gauges/>

对于普通驾车者来说，车速表和燃油指示器是主要的感兴趣的仪表。高性能车或改装车的车主往往喜欢获得更多关于汽车行驶方式的信息。[JustinN1]坚定地站在这个阵营中，[为他的斯巴鲁 WRX STi](https://www.instructables.com/id/Wifi-Enabled-OLED-ESP32-Car-Gauges/) 制造了一些支持 WiFi 的仪表。

这些仪表在 ESP32 平台上运行，选择 ESP32 平台是因为其 WiFi 硬件和 Arduino 平台的易用性。这使得编程变得轻而易举，与智能手机的接口也很容易。选择有机发光二极管显示器是因为它们在白天和夜晚都具有良好的可视性，这对于汽车应用非常重要。

[JustinN1]开发了一个增压/真空表和一个油压表，两者都有助于监控发动机的运行情况。测量增压就像使用现成的模拟气压传感器一样简单。油压传感器是一个电阻部件，必须通过电阻分压器连接，以产生模拟电压供 ESP32 读取。

Github 上有代码，甚至有一个版本，当你进入更高的提升级别时，[会露出一张咧着嘴笑的脸。还有一系列适合各种安装选择的外壳，有助于赋予压力表更完美的外观。我们也看到了其他规格的产品，](https://github.com/stirobot/ESP32BoostFaces)[，比如这个铃木摩托车的档位指示器](https://hackaday.com/tag/gear-indicator/)。休息后的视频。

 [https://www.youtube.com/embed/F1PGuGUun_s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/F1PGuGUun_s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

