# 精确的时间在你的圆周率上，极端的方式

> 原文：<https://hackaday.com/2019/06/26/accurate-time-on-your-pi-the-extreme-way/>

Raspberry Pi 是一款功能极其丰富的小型电脑，但即使是其最狂热的粉丝也会承认，它的硬件在某些领域略有欠缺。其中之一是在计时领域，小板子没有实时时钟。用户必须依赖板载晶体振荡器，它作为微处理器时钟已经足够好，但受温度变化的影响，而不是长期时钟。

[Tobias mdel]以一种相当不寻常的方式解决了这个问题，他在旧的 Pi 模型上完全取消了晶体振荡器，而是使用了一个来自 GPS 源的时钟。他使用的信号源是一个[利奥博德纳尔微型精密 GPS 参考时钟](http://www.leobodnar.com/shop/index.php?main_page=product_info&cPath=107&products_id=301&zenid=6910084fdac70aedf1eabef8706c4c6d)，其中包括一个低抖动合成器，可以设置为 Pi 所需的 19.2 MHz 时钟。出乎意料的是，他还需要一个简单的 LC 低通滤波器，这是他在一片 PCB 材料上制作的，因为 Pi 起初似乎是拾取谐波频率。Pi 现在有了一个足够稳定的时钟，可以用于 WSPR 传输等任务，而不需要不断参考 NTP 或其他定时源来保持其正常运行。

这是一篇简短的文章，但它为[带来了一个进一步的链接](https://www.satsignal.eu/ntp/Raspberry-Pi-NTP.html)来讨论 Pi 上的不同时间同步技术，包括使用内核模块来与更常见的 GPS 衍生的 1PPS 信号同步。我们以前没有见过其他人对 Pi 做这种特殊的修改，但是相反的[我们见过 Pi 为其他东西提供 RF 时间参考](https://hackaday.com/2018/09/10/no-signal-for-your-radio-controlled-watch-just-make-your-own-transmitter/)。