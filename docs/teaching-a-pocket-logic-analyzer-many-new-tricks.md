# 教一个袖珍逻辑分析仪(许多)新花样

> 原文：<https://hackaday.com/2020/10/01/teaching-a-pocket-logic-analyzer-many-new-tricks/>

几年前，针对黑客和制造商群体的低成本袖珍数字示波器开始进入市场，并获得了相当多的追随者。虽然很少有人会认为它们是一个合适的板凳范围的替代品，但它们足够便宜和方便，很难抱怨。制造商显然希望扩展这一概念，因为我们现在看到类似价格和大小的逻辑分析仪从通常的来源中出现。

[Gabriel Valky]得到了一个低于 100 美元的型号 LA104，并认为股票软件不太好用。因此，他启动了一个项目，为价格低廉的小工具创建一个新的开源固件，极大地扩展其核心功能。代码甚至被移植到了一些数字示波器上，因为事实证明(也许并不令人意外)，它们在内部并没有被移得太远。

[![](img/ef50f87470d26c54ffcf91bd785aa329.png)](https://hackaday.com/wp-content/uploads/2020/09/la104fw_detail.png)

Controlling addressable LEDs with the LA104.

在休息后的视频中，[Gabriel]展示了一些令人印象深刻的无线电技巧，在混音中添加了一个小型 CC1101 收发器。这使得他改进的 LA104 能够在 300–900 MHz 范围内扫描和解码流行的 RF 协议。他的软件甚至允许接收到的数据包被修改并重新传输，他通过向无线气象站发送一个假的温度信号来演示这一点。

但这只是开始。仔细阅读 GitHub 页面，他的替换固件显示了这个项目已经包含了多少功能。例如，它可以用来控制 WS2812 LED 灯条、生成任意 PWM 信号、记录温度传感器的数据、与 MIDI 设备接口以及扫描 I2C 设备。这些功能中的许多可以通过利用现代浏览器和 WebUSB 在计算机上控制。

[Gabriel]为 LA104 提出的替代固件确实是一个不可思议的成就，提升了一个已经很有趣的套件。能够将所有这些功能打包到一个足够小和便宜的包里，对移动中的黑客来说是一个非常有吸引力的前景。

 [https://www.youtube.com/embed/Gwyi00NKBNg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Gwyi00NKBNg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

