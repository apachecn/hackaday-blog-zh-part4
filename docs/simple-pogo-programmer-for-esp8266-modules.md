# 用于 ESP8266 模块的简单 Pogo 编程器

> 原文：<https://hackaday.com/2019/12/07/simple-pogo-programmer-for-esp8266-modules/>

像 Wemos D1 Mini 和 NodeMCU 这样的 ESP8266 开发板是快速启动和运行一次性项目的绝佳方式，但它们的尺寸和相对复杂性意味着它们不一定是短期生产硬件的好选择。另一方面，编程裸露的 ESP 模块可能是一件痛苦的事情。但是多亏了[格雷格·弗罗斯特]，[闪现那些小板子变得容易多了。](https://www.thingiverse.com/thing:3995162)

[![](img/fa4d228cdd57bae373b79ca48e0dc759.png)](https://hackaday.com/wp-content/uploads/2019/11/pogoesp_detail.jpg) 他的 3D 打印设计使用弹簧针安全地连接到电路板的齿形边缘，这也在编程过程中保持它的位置。在背面，只有几根跳线和几个电阻，最终导致 FT232R FTDI 板，实际上将芯片连接到计算机，以便您可以对其进行编程。

我们希望看到一个封闭布线的背板，也许是一个替代版本，删除 FTDI 板的空间，支持一排插头引脚。对基本设计的简单修改应该会让[Greg]或其他人感到如此倾向。但即便如此，这也是一个很棒的小程序，可以很容易地、廉价地获得和组装。

这个[并不是我们见过的第一个 3D 打印的 ESP8266 程序员](https://hackaday.com/2018/03/27/3d-printed-esp8266-programming-jig/)，[还有一些即兴版本](https://hackaday.com/2019/05/18/breakout-board-becomes-pogo-pin-programmer/)组装起来甚至更便宜，但这个设计有一定的专业外观，我们认为它会放在你家的长凳上。