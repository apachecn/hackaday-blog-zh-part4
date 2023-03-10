# 用实时动态随机存取存储器窥探星联

> 原文：<https://hackaday.com/2022/09/23/snooping-on-starlink-with-an-rtl-sdr/>

随着越来越多的 Starlink 卫星群在我们头顶呼啸而过，你可能会有开始尝试高速互联网服务的冲动。但每月 100 美元或以上加上硬件，对我们许多人来说，进入门槛有点令人生畏。不过，不用担心——如果你感兴趣的只是跟踪[埃隆]的鸟，那么这实际上是一项非常简单的工作。

现在，我们并不是说你可以通过这个设置连接到 Starlink 并获得互联网服务，当然，这个有趣的名字[saveitforparts]也不是。相反，他的装置只是接收来自 Starlink 卫星的信标信号，这本身就很有趣。硬件包括他的“Picorder”移动设备，它有一个树莓 Pi、一个小液晶屏和一系列传感器，包括一个 RTL-SDR 加密狗。为了接收卫星信号，他使用了非常便宜的通用 Ku 波段 LNB，即低噪声块下变频器。它们通常被发现在卫星电视碟形天线的焦点上，但在这种情况下，不需要任何碟形天线——只需用电动注射器给它通电，并将其指向天空。信号以瀑布模式出现在 Picorder 的显示器上；奇怪的是，瀑布的痕迹看起来与卫星在夜空中形成的图案非常相似，[让天文学家们大为惊愕](https://hackaday.com/2019/11/20/starlink-satellites-posing-issues-for-astronomers/)。

当然，你不一定要有微型计算机才能窥探 Starlink——任何笔记本电脑和 SDR 都应该可以工作，尽管[saveitforparts]这样做有麻烦。按照下面的视频复制结果应该不会有太大的困难，其中也有一些为便携式操作的 LNB 供电的技巧。

 [https://www.youtube.com/embed/5cwEkhFdXGw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5cwEkhFdXGw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via[RTL-SDR.com](https://www.rtl-sdr.com/detecting-starlink-satellites-with-a-portable-raspberry-pi-rtl-sdr/)