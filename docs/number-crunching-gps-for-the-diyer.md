# 数字运算全球定位系统为 DIYer

> 原文：<https://hackaday.com/2020/07/02/number-crunching-gps-for-the-diyer/>

我们中的许多人都有理由在项目中加入 GPS，无论是因为我们需要一个精确的时基，还是仅仅想知道该死的东西在哪里。通常，这包括插入一个便宜的模块，并确保天线有一个良好的天空视野。[Mike]想要更深入地研究，找出解码 GPS 信号和计算定位的方法。

[迈克]的调查结合了几种调查方法。在解码直播无线电信号方面，他选择了 KiwiSDR 软件定义无线电。结合 Digilent Nexys 2 FPGA，现在可以将直播数据从空中快速传输到 PC 进行解码。与此相呼应的是，[Mike]使用了在英国诺丁汉捕获的原始 GPS 数据样本来测试他的代码。经过多次实验，[迈克]能够用 700 行 C 代码解码数据。解码三分钟的数据需要一整夜，但是进一步的发展使得速度提高了 200 多倍。令人好奇的是，[Github 上有将原始 ADC 样本转换成实际定位的代码。](https://github.com/hamsternz/Full_Stack_GPS_Receiver)

有了丰富的网上资源和合适的硬件，[Mike]成功地实现了他的目标，并且准确地找到了他家的位置。另外，整个项目的灵感来自于[2013 年这些页面上发布的一个类似项目！](https://hackaday.com/2013/05/17/homebrew-gps-gets-%c2%b11-meter-resolution-with-a-raspberry-pi/)如果你正在做自己的卫星项目，[一定要给我们写信。](http://hackaday.com/submit-a-tip)