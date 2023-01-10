# 茶叶袋库存管理的现代解决方案

> 原文：<https://hackaday.com/2019/02/20/a-modern-solution-to-tea-bag-inventory-management/>

英国以礼仪和好客而闻名。除了在招待客人时用完茶包之外，很少有什么情况能让英国人绷紧的上唇颤抖。谢天谢地，[绅士制造者]在这里，名副其实地拥有一个有用的茶叶监控器，确保你再也不会被抓到。

这个被称为 Intelli-T 的系统通过重量来监控茶叶库存。Arduino Uno 结合 HX711 IC 监控安装在罐下的称重传感器，盖子上有一个簧片开关。打开和关闭茶叶罐后，Arduino 会进行测量，确定茶叶库存是否已降至临界水平以下。如果情况很糟糕，通过串口连接的树莓派会向住户发出紧急警告。如果有足够的茶，树莓派将提供一个有用的茶事实，以进一步教育用户关于神圣的饮料。

鉴于 Raspberry Pi 的强大功能，这是一个有趣的项目，并且具有进一步特性的空间。再做一点工作，就可以在网上自动订购更多的茶叶，或者通过 IFTTT 这样的服务发送警报。我们以前见过[绅士制造者]独特的英国风格，比如[告诉你天气的伞](https://hackaday.com/2018/12/25/the-umbrella-that-tells-you-the-weather/)。休息后的视频。

 [https://www.youtube.com/embed/_YBjk5vVYDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_YBjk5vVYDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

