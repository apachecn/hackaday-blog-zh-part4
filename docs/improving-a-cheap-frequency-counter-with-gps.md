# 用 GPS 改进廉价频率计

> 原文：<https://hackaday.com/2019/05/23/improving-a-cheap-frequency-counter-with-gps/>

对于那些经常处理时变信号的人来说，频率计数器是非常有用的工具。从便宜的易贝特价商品到昂贵的实验室级硬件，种类繁多。[itakeyourphoto]有一个价格较低的计数器，[并决定在 GPS](https://www.youtube.com/watch?v=1Dp1Yu-KMns) (Youtube 链接，嵌入下面)的帮助下做一些改进。

廉价频率计数器的根本弱点通常是内部基准，所有其它信号都是根据它来测量的。这越精确，计数器就越精确。[itakeyourphoto]确定了一个产生相当好的参考频率的好方法是使用 uBlox GPS 模块。一旦锁定卫星，它可以使用数控振荡器以良好的精度输出高达 15MHz 的任何频率。

问题中的廉价频率计数器使用 13 MHz 内部基准电压，因此 uBlox 模块被编程为与之匹配。[itakeyourphoto]报告称，它比他的高端 GPS 振荡器更好，显示出非常小的漂移或其他异常。

我们看到许多时钟使用 GPS 来获得精确的时间，[，但我们也看到一些项目试图走得更远。休息后的视频。](https://hackaday.com/2019/05/11/whats-more-accurate-than-a-gps-clock-the-openppc-gps-clock/)

【感谢 jafinch78 的提示！]

 [https://www.youtube.com/embed/1Dp1Yu-KMns?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1Dp1Yu-KMns?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

