# 通过软件定义的无线电监控 SpaceX 火箭发射

> 原文：<https://hackaday.com/2021/03/11/monitor-spacex-rocket-launches-with-software-defined-radio/>

最近，业余无线电爱好者社区活动激增，尤其是在软件定义无线电(SDR)领域，因为人们发现，一个小型廉价的电视调谐器可以完成以前只有昂贵设备才能完成的任务。这些卡的一个常见构造是监控空中交通，它通过无线电以数据包的形式发送关于他们飞行的数据，现在可以很容易地接收和解码。原来，另一种类型的交通工具，SpaceX 的猎鹰 9 号飞船，也通过无线电报告数据，并且通过一些稍微升级的硬件[，有可能以类似的方式“监听”这些飞行](https://www.rtl-sdr.com/receiving-space-x-falcon-9-telemetry-with-a-hackrf-and-1-2m-satellite-dish/)。

Reddit 用户[derekcz]和[Xerbot] 在猎鹰 9 号最近一次发射期间使用了一个 HackRF 模块来监听它的数据传输。虽然与用于监听飞机的 RTL-SDR 加密狗相比，HackRF 是一种更昂贵的设备，但它的能力也更强，范围从 1 MHz 到 6 GHz。使用这个 SDR 外围设备以及一个 1.2 米的重新设计的卫星碟形天线，两人能够拦截飞行中的火箭的无线电传输。从那里，它们被 GNU Radio 记录下来，转换成二进制数据，然后翻译成文本。

看起来似乎数据反馈包括了许多不同的元素，包括时间、位置信息和其他关于火箭飞行的实时数据。这是一个很好的构建，展示了软件定义无线电的广泛吸引力，如果你想开始使用，很容易[获得一个便宜得多的加密狗，并将其用于各种应用，如这种](https://hackaday.com/2020/10/22/tracking-boats-and-ships-in-real-time-at-the-same-time/)。去看看[汤姆·纳尔迪]关于[过去七年的 RTL-SDR](https://hackaday.com/2019/07/31/rtl-sdr-seven-years-later/)的文章，了解一下最新进展。

感谢[阿德里安]的提示！