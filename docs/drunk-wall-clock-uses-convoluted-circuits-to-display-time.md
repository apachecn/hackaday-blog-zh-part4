# 醉挂钟使用错综复杂的电路来显示时间

> 原文：<https://hackaday.com/2021/09/20/drunk-wall-clock-uses-convoluted-circuits-to-display-time/>

在 Hackaday，我们永远也看不够奇怪的时钟，我们很高兴看到[丹·奥谢]的创造，称为 [Wifi-Telnet-FPGA-NTSC 醉挂钟](https://hackaday.io/page/11213-wifi-telnet-fpga-ntsc-drunk-wall-clock)。这个词准确描述了它的功能:该设备的核心是一个 ESP32，它使用 WiFi 连接到树莓派。然后，它远程登录到系统，登录，并使用 Linux `date`命令请求当前时间。到目前为止，如此平凡。

“FPGA”部分变得更奇怪了:ESP32 连接到一个 [VGA1306 板](https://hackaday.com/2018/03/11/fpga-magic-puts-little-embedded-screens-up-on-the-big-screen/)。这是一个带有 FPGA 的小 PCB，模拟有机发光二极管显示器，并将图像输出到 VGA 连接器。[Dan]本可以简单地连接一个 VGA 显示器，但却采用了另一层复杂性，只使用三个电阻，将 VGA 信号转换为类似复合视频的信号。由此产生的“NTSC”信号被送入一个显示时间的小型 TFT 显示器。

这个时钟被贴上了“喝醉”的标签，因为重复运行`date`命令并解析其输出的过程很慢，而且容易打嗝，导致显示的秒以某种不稳定的方式前进。这非常符合时钟的整体美学，时钟由一堆用电缆扎带和电工胶带固定在一起的 PCB 组成。它安装在回收木的圆形面板上，是任何黑客实验室的美丽墙壁装饰品。

我们喜欢这种以复杂的方式完成简单任务的项目，而且不缺乏不必要的复杂时钟，无论是物理绘制时间还是使用机器学习数据。但是如果你只是喜欢你的电子设备外露的时钟，看看这个[自由形式的 LED 时钟](https://hackaday.com/2020/05/09/beautiful-free-form-led-clock-recreates-20-year-old-weekend-project/)或者这个简洁的[电路雕塑时钟](https://hackaday.com/2020/06/08/circuit-sculpture-clock-goes-pew-pew/)。

 [https://www.youtube.com/embed/Ka1GHB7hSRk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ka1GHB7hSRk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

