# 2022 年 Hackaday 奖:这张交互式空气质量地图让看不见的东西变得可见

> 原文：<https://hackaday.com/2022/10/11/hackaday-prize-2022-this-interactive-air-quality-map-makes-the-invisible-visible/>

空气质量会对你的健康产生很大影响，但这并不总是你能看到的。艾哈迈德·奥耶努加想要让空气质量变得更加有形，他开发了一个[交互式空气质量地图](https://hackaday.io/project/187662-the-interactive-air-quality-map)。

利用可寻址的 led 和丙烯酸面板，[ Oyenuga ]的地图用与空气质量读数的定性值相对应的颜色照亮了他所在州(拉各斯)的不同区域。当您触摸地图的特定区域时，地图边缘的颜色键会变成读数。

地图的大部分功能都是由 Arduino WiFi 1010 处理的，但电容触摸是在使用 ATSAMD21J17 设计的定制板[ Oyenuga ]上运行的。[ Oyenuga ]正在通过 DesignSpark 环境传感器开发套件(ESDK)获取空气质量数据，然后使用[反向地理编码](https://en.wikipedia.org/wiki/Reverse_geocoding)获取 GPS 数据，并将其转换为地图可以理解的位置。

如果你对监测空气质量的不同选项感兴趣，这些选项可以输入到这样的地图中，为什么不看看这个[劳拉空气质量监测器](https://hackaday.com/2022/08/30/lora-air-quality-monitor-raises-the-bar-on-diy-iot/)甚至是一个[移动空气质量监测器](https://hackaday.com/2021/12/13/measuring-air-quality-using-mobile-sensors-for-the-masses/)。

 [https://www.youtube.com/embed/JFPuA-AhaiU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JFPuA-AhaiU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)