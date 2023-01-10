# Web 界面控制数码管时钟

> 原文：<https://hackaday.com/2019/05/05/web-interface-controls-nixie-tube-clock/>

我们喜欢这里的钟表，也喜欢谢妮电子管。这两者的结合似乎是显而易见的。Reddit 用户[vladco]用 ESP8266 的现代风格制作了一个[极简的数码管时钟](https://goo.gl/photos/xAqDbSyT5gKFA5jb8)。

建造从谢妮电子管开始，俄罗斯的 in4，每个电子管都安装在自己的小电路板上。每块木板都用链条连接在一起，并安装在一个木架上。该框架安装在一个漂亮的木箱内，该木箱是在 Fusion 360 中设计的，并在当地的 hackerspace 由橡木铣成。

这个案子没有任何控制。没有按钮或旋钮。该时钟通过 EPS8266 设置，它获取时间并更新设置每个电子管上数字的移位寄存器。时钟在晚上变暗，所以不那么亮。[vladco]编写了一个 web UI 来设置时间并与试管进行交互。

外壳和电路板的代码和文件[可在线获取](https://github.com/putyn/nixie-clock)。结果是一个漂亮的，简约的时钟放在你的桌子上。现场有大量的时钟建造，几个由谢妮电子管建造，包括[另一个带 ESP8266 的数码管](https://hackaday.com/2017/11/10/esp-powered-nixie-clock-knows-the-time/)时钟，[另一个](https://hackaday.com/2017/10/13/hackaday-prize-entry-iot-nixie-clocks/)。

via [Reddit](https://www.reddit.com/r/electronics/comments/bhig9p/russian_in4_in_a_hard_wood_case_with_an_esp8266/?st=juydznkx&sh=477106d5)