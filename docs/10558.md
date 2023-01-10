# Miata 科幻数字仪表板

> 原文：<https://hackaday.com/2021/06/27/miata-sci-fi-digital-dash/>

对于一个项目，你能做的最难但有时也是最好的事情之一就是走开。[Jroobi]花了数百个小时为他的 MX5 Miata(视频，嵌入下方)制作数字 dash，在花了太长时间追逐 I2C bug 后，他做出了一个艰难的决定，离开一段时间。然而，截至 2021 年 5 月，[Jroobi]回到项目后发现电源供应不足，并导致限电，从而导致事故。

总而言之，这是一项不可思议的工程。从描述所有不同状态的大规模代码库到有品位的图形设计，一切都是精心完成的。受《星际迷航》启发的主题和对细节的关注真正体现在转速表的不同模式中。基于发动机温度的动态软转速限制特别巧妙。

在这辆定制破折号的引擎盖下，是两辆 Ardunios 在表演。中央媒体控制台通过宽大的触摸屏提供了更多的控制，而仪表组显示大部分数据。他们通过 I2C 互相交谈，并与车内的其他部件进行通信，如 RGB 驾驶室照明和 TEIN 电子悬架减震器。燃料和温度水平以电压水平的形式出现，可通过 ADC 读取。给定车轮尺寸和车辆中的变速器，档位是基于 rpm 和速度计算的。

这是一项非凡的爱的劳动，如果你受到启发进一步升级你的 Miata，你可能想看看如何[在发动机上添加碳水化合物](https://hackaday.com/2019/08/08/putting-carbs-on-a-miata-because-its-awesome/)或在仪器中 [RGB 灯环](https://hackaday.com/2021/04/29/rgb-led-rings-teach-old-dash-new-tricks/)。

 [https://www.youtube.com/embed/v4QwvA_xGU4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/v4QwvA_xGU4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

