# 找到合适的黑客是成功的一半

> 原文：<https://hackaday.com/2021/09/18/finding-the-right-hack-is-half-the-battle/>

有时候你只是运气好。我的清单上有一个项目已经有很长时间了，这个项目我已经推迟了几个月，因为我讨厌其中的一部分——敏感、高精度的模拟测量。然后，出乎意料地，我发现了正确的窍门，我的问题消失得无影无踪。感谢黑客之网！

该项目是一个低真空调节器，用于玻璃纤维叠层的“装袋”。我需要的是读取压力传感器的某种方法，并相应地打开和关闭真空泵。行业标准的真空计是简洁的设备，本质上是一个微小的应变仪，位于真空侧和大气侧之间的薄膜上，封装在一角硬币大小的封装中。(这是一个应变仪是铺垫，但我当时不知道。)几年前，我花 15 美元买了一台，它就放在我的桌子上，等待它的模拟电路。

MPX2100 采用 12 V 电源供电，在 6 V 失调电压的基础上输出约 40 mV 的信号。该电压水平不适合现代 3.3 V 微控制器 ADC，如果我在其上放置一个分压器，分辨率会受到 6 V 信号的影响。这意味着将某种仪表放大器电路组合在一起，以消除 6 V 电压，并为 ADC 放大 40 mV 电压。我在网上找到的电路都要求 1%的电阻值，我没有，和轻度特殊运算放大器。不好玩，至少对我来说。所以它就在那里。

[![Picture of sketchy-looking vacuum apparatus.](img/d62cecb43053d2ad7462e45a163f95a2.png)](https://hackaday.com/wp-content/uploads/2021/09/DSCF2554_thumbnail.png)

Cut the blue wire or the red wire? HX711 module and pressure sensor on the left.

直到我遇到了这个项目，这个项目用一个零件在模拟丛林中弯刀，而这个零件恰好是我手头上的一个。真空压力传感器是一种应变仪，像惠斯通电桥一样设置，就像用称重传感器称重一样。解决办法？HX711 是一款称重传感器 ADC 芯片，在每台廉价电子秤或网上售价不到 1 美元。唯一的另一个技巧是找到一个低压压力传感器来配合它，但事实证明[也很容易](http://www.datasheetcafe.com/md-ps002-datasheet-air-pressure-sensor/)，我在两天内就交付了一个。

总之，这个项目花了几个月的拖后腿，但只有几次点击和五分钟的焊接，一旦我有了正确的想法。如果你正在制造数以百计或数以百万计的这类设备，工业应用和制造商的应用笔记都是有意义的，在这种情况下，制作硬件原型的一次性成本可以摊销，但使用重量级芯片的黑客解决方案只是一次性的。这只是表明分享我们的技巧和诀窍是多么有用——你不会从行业中得到这些。所以[把你的成功故事](https://hackaday.com/submit-a-tip/)和你有用的失败也发给我们，并阅读更多 Hackaday！

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!