# 自制射电望远镜包脉冲星

> 原文：<https://hackaday.com/2022/05/25/homebrew-radio-telescope-bags-pulsar/>

当一个人考虑探测脉冲星的可能性时，他会想到大型碟形天线和一架又一架的灵敏接收器、滤波器和数字信号处理器。但是有不止一种方法可以捕捉到这些天体信标发出的有规律的无线电脉冲，如果你知道你在做什么，一个小型卫星天线和一个 RTL-SDR 加密狗就足够了。

诚然，[Job Geheniau]在探索无线电宇宙方面有很多经验。他的网站上有一长串使用他的“JRT”或“乔布斯的射电望远镜”所获得的观察和成就该仪器看起来像一个家酿者的梦想，有一个 1.9 米的卫星电视碟形天线和精密的方位角-仰角旋转器。喇叭天线后面是一对低噪声放大器和带通滤波器，用于按摩射电天文学常用的 1,420 MHz 信号，外加一个 Nooelec 智能 SDR 加密狗和一个 Airspy Mini。一切都通过远程控制运行，因为位于他家农场的天线的干扰要低得多，距离他在海牙的家 50 公里。

至于脉冲星，它被命名为 PSR B0329+54，它是一颗 500 万年前的中子星，位于骆驼星座，距离我们大约 3500 光年。这是一颗特征明显的脉冲星，每隔 0.71452 秒发出一次脉冲，但通常要用非常大的天线才能观测到。[约伯]的观察报告包含了他所使用的方法和软件的许多细节，虽然这些数据对于不经意的观察者来说很不清楚，但看起来肯定是他收集的。

我们之前已经看过不少 DIY 射电天文学项目，既有[大的](https://hackaday.com/2022/03/22/tune-your-dish-antenna-like-a-pro/)也有[小的](https://hackaday.com/2018/10/13/tiny-telescope-for-simple-radio-astronomy/)，但是这个项目的成就确实令人印象深刻。

[via[RTL-SDR.com](https://www.rtl-sdr.com/pulsar-b032954-detected-with-a-1-9m-dish-and-rtl-sdr/)