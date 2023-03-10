# 分裂皮瓣时钟保持时间感谢自定义频率转换器

> 原文：<https://hackaday.com/2019/06/23/split-flap-clock-keeps-time-thanks-to-custom-frequency-converter/>

为什么有人会像[mitxela]在建造[这种定制 PLL 频率转换器](https://mitxela.com/projects/phase-locked_inverter)时所做的那样，花那么多精力去复活一个 20 世纪 70 年代的分体式时钟呢？我们不确定，但我们喜欢这个结果。

这座钟是对 1993 年经典电影《土拨鼠日》中道具的再创造，使用普通的声卡等设备，只播放“我给你买了宝贝”。但有趣的部分是让时钟机制保持体面的时间。该时钟来自美国，需要 60 赫兹的 120 伏交流电，而不是英国标准的 240 伏交流电，50 赫兹。电压差可以很容易处理，但频率不匹配导致时钟运行速度慢得令人无法接受。

那时[mitxela]全力以赴，设计了一个定制电路，将 50 赫兹的市电转换为 60 赫兹。更重要的是，他决定将他的合成波形锁定到电源电流，以利用以长期频率控制而闻名的电力生产商。这篇文章详细介绍了锁相环(PLL)的设计，它使用 ATtiny85 来监控市电电源的上升沿，并产生 PWM 信号，从而每 5 个周期输出 6 个周期。结果是钟现在走得很准，他也学到了一点东西。

如果[mitxela]这个名字看起来很熟悉，那可能是因为我们以前展示过他的许多令人敬畏的构建。从可笑的大规模焊接到[一台热敏打印机宝丽来](https://hackaday.com/2018/04/16/polaroid-gets-thermal-printer-and-raspberry-pi/)到[一个莫尔斯转 USB 键盘](https://hackaday.com/2017/01/25/tiny-morse-code-usb-keyboard/)，他总是在做一些很酷的事情。