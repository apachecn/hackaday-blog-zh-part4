# 廉价的传感器和一个 SDR 监控着这个丝干农场的状况

> 原文：<https://hackaday.com/2019/09/14/cheap-sensors-and-an-sdr-monitor-conditions-in-this-filament-drying-farm/>

我们不知道(斯科特·m·贝克)把哪里叫做家，但那肯定是一个相当潮湿的地方。毕竟，他已经在花哨的真空储存容器上投资了相当多的钱来保持他的 3D 打印机细丝干燥，结果是这个充满传感器的细丝干燥农场。

[Scott]不满足于仅仅使用这些 [PrintDry 容器](https://www.printdry.com/product/vacuum-sealed-filament-container/)而不知道里面发生了什么。经过一点清洁和润滑，让所有的容器都能工作，他开始制造传感器。他选定了一个无线系统，每个集装箱都有一个 BME280 温度/湿度/压力传感器和一个 syn 115 315 MHz ISM 频段发射机模块。这些与 ATtiny85 一起放入一个紧凑的 3D 打印盒中，盒中装有少量二氧化硅干燥剂。发射器的编程符合 ISM 频段的规定——无需[违反这些规定](https://hackaday.com/2019/05/15/the-great-ohio-key-fob-mystery-or-honey-i-jammed-the-neighborhood/)——而接收器只是一个 SDR 加密狗和运行 rtl_433 的树莓 Pi。下面的长视频详细介绍了设计和施工。

这些真空容器背后的想法似乎是抽出潮湿的空气，并防止它回来。但是[斯科特]很快从他的遥测技术中了解到，按照指示行事只会产生大约 2700 英尺(823 米)高度的等效大气压力——不完全是硬真空。但正如[斯科特]指出的那样，这足以获得一个良好、紧密的密封，他的数据显示，随着时间的推移，相对湿度会降低并保持恒定。

 [https://www.youtube.com/embed/dPXWNPLYEuo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dPXWNPLYEuo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

