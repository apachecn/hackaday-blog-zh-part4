# 有了这个通知程序，再也不会错过门铃了

> 原文：<https://hackaday.com/2020/03/01/never-miss-a-doorbell-with-this-notifier/>

[路径]告诉我们，他悲惨地错过了一次精酿啤酒送货上门，并发誓再也不会让这种事情发生。他的问题是，他错过了门铃，导致了一个讨厌的快递员的注意。他的解决方案？一个由 ESP8266 驱动的门铃探测器，既能给他发短信，又能把每次按门铃的情况记录到一张谷歌表上。

门铃检测令人惊讶，但简单且无干扰，他没有通过某种接口将 GPIO 线连接到按钮本身，而是在他的 ESP8266 板上添加了一个簧片开关，并使用它来检测门铃螺线管的磁场。这是一种方便的方法，但只适用于老式的铃铛。

当门铃响起时，磁场触发簧片开关，反过来，运行在 ESP 上的草图调用 IFTTT，if TTT 触发 SMS 并写入记录每次门铃激活的 Google Sheets 文档。

ESP8266 [似乎是门铃 automatprs](https://hackaday.com/2019/01/07/building-an-esp8266-doorbell-on-hard-mode/) 的一个受欢迎的选择，可能是因为它的内置网络和低价格，但它不是唯一的选择。这种光耦合器感应的努力例如[使用粒子氙](https://hackaday.com/2019/10/21/an-optocoupler-Adoorbell-notifier/)。