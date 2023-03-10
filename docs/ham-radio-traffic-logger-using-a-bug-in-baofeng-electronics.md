# 业余无线电流量记录器使用的是宝丰电子的窃听器

> 原文：<https://hackaday.com/2021/06/10/ham-radio-traffic-logger-using-a-bug-in-baofeng-electronics/>

宝丰收音机通常是新的业余无线电爱好者购买的第一批产品之一，因为它功能不错，价格低廉。它们远非完美，但只要有一点创造性的灵感，就有可能让这些怪癖对你有利。每当 LCD 背光打开时，耳机输出就会发出响亮的爆音，利用这一点，[威士忌酒吧]使用 ESP8266 构建了一个[无线电流量计数器](http://www.whiskeytangohotel.com/2021/05/2m-70cm-ham-radio-traffic-logger.html)。

每当收音机调谐到的一个频率上有信号传输时，背景灯就会点亮。将音频输出连接到示波器，每当这种情况发生时，[WhiskeyTangoHotel]测量到一个 5V 的尖峰。ESP8266 使用一对串联二极管将电压降至安全水平，检测电压尖峰，并通过 IFTTT 用时间戳更新谷歌电子表格。

这给了[威士忌酒吧]关于有多少流量通过当地甚高频中继器的经验数据，但如果黑客本身是真正的动机，我们不会责怪他们。

当然，这也是对 RTL-SDR 的一个完美应用，它可以让你在软件中做以上的事情和更多的事情。添加一点人工智能，你甚至可以[提取呼号](https://hackaday.com/2018/10/09/using-ai-to-pull-call-signs-from-sdr-processed-signals/)。RTL-SDR 也是学习[射频调制](https://hackaday.com/2020/01/28/rf-modulation-crash-course-for-hackers/)的好工具。

通过 [PE1RQM](https://www.pe1rqm.nl/techniek-info/baofeng-uv-5r-uv-5re-review/) 的 UV5-R 图像