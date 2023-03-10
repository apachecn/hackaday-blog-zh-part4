# 通过开源的自动无线电探空仪跟踪

> 原文：<https://hackaday.com/2019/02/10/automated-radiosonde-tracking-via-open-source/>

世界各地的气象组织定期发射气象气球，作为预测周末是否会下雨的工作的一部分。它们的有效载荷被称为无线电探空仪，这些气球在整个飞行路线上传送遥测和定位数据。全球的业余爱好者已经投入时间和精力来跟踪和解码这些信号，[现在，由于无线电探空仪自动接收](https://github.com/projecthorus/radiosonde_auto_rx)，这一切都可以自动完成。

该项目的基础是 RTL-SDR，这是每个人都喜欢的低成本软件无线电接收机。在这种情况下，软件首先被用来寻找潜在的无线电探空仪信号，然后解码它们并将结果上传到各种在线服务。其中一些是为简单的跟踪而设计的，而另一些是为现场追踪和回收操作而设计的。目前，该软件仅涵盖 3 种无线电探空仪，但该团队渴望扩展该项目，并请求捐赠其他无线电探空仪用于研究目的。

该团队最近在 linux.conf.au 上就项目进行了一次演讲，详细介绍了无线电探空仪数据的解码和跟踪。如果你急于尝试，下载软件，拿起你的电视加密狗，开始破解。[你也可以考虑追踪立方体卫星。](https://hackaday.com/2018/06/01/tracking-cubesats-for-25/)休息后的视频。

[via [crazyoperator](https://crazyoperator.wordpress.com/2019/01/30/hunting-weather-ballons-radiosondes-with-open-source/) ]，感谢 Slds Ernesto 的提示！

 [https://www.youtube.com/embed/YBy-bXEWZeM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YBy-bXEWZeM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

