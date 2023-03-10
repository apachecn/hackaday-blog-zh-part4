# 2022 年 Hackaday 奖:紧凑型太阳能跟踪系统不会破产

> 原文：<https://hackaday.com/2022/08/28/hackaday-prize-2022-compact-solar-tracking-system-doesnt-break-the-bank/>

如果你需要从太阳能电池板中榨出每一瓦特的能量，你可能会想看看太阳能跟踪系统。不幸的是，它们通常很大，很重，而且很贵。作为替代，[JP Gleyzes]已经组装了一个 DIY 太阳能跟踪系统，旨在解决这些问题。

从黑色星期五销售期间购买的 100 W 柔性太阳能电池板开始，[JP]首先使用 20 mm PVC 管和几个 3D 打印支架创建了一个简单的框架。它安装在一个木制底座上，带有印刷的蜗轮旋转机构，由步进电机驱动。倾斜由螺杆制成的丝杠控制，连接在木制底座和太阳能电池板顶部之间，也由步进电机驱动。

为了实现更高的效率，[JP]还开发了一款 [MPPT](https://hackaday.com/2022/08/03/maximum-power-point-tracking-optimizing-solar-panels/) 充电控制器和配套应用程序，该控制器使用 ESP32、经过改进的 20 A 降压转换器和电流传感器模块。ESP32 还控制步进电机。使用日期、时间和系统的 GPS 位置确定太阳能电池板[的最佳角度。[JP]还创建了一个简单的 Android 应用程序来校准面板的起始位置。](https://hackaday.com/2012/01/03/arduino-heliostat-calculates-the-position-of-the-sun/)

这个项目是 2022 年 Hackaday 奖的环保能源挑战的决赛项目，所有的细节都可以在你的项目页面上找到。从系统的规模来看，我们怀疑未来的迭代会更小。

 [https://www.youtube.com/embed/tAy-2GW3cyU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tAy-2GW3cyU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/XpKSuz8YUdo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XpKSuz8YUdo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)