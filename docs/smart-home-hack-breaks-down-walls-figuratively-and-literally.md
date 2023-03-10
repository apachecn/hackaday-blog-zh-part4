# 智能家庭黑客打破墙壁比喻和字面意思

> 原文：<https://hackaday.com/2021/09/15/smart-home-hack-breaks-down-walls-figuratively-and-literally/>

你准备好接受一个糟糕的硬件支持、无能的承包商和糟糕的编码的故事了吗？看看[Neighborino]精彩的文章就知道了，他在文章中详细描述了他对智能家居的追求。

[邻居]的智能家居系统控制窗户、百叶窗、插座和 HVAC。但到 2015 年这栋高层公寓准备入住时，智能家居控制器已经显示出它们的年龄了。你看，承包商已经安装了一个应用程序来运行股票 Galaxy Tab 3 硬件上的家庭可编程逻辑控制器(PLC)。是的，那是一款最初于 2013 年发布的平板电脑。然后，他们将平板电脑嵌入每套公寓的墙壁，注定房主将永远依赖供应商。

没过多久，[邻居]和他们的居民们就开始处理稳定问题了。三星和谷歌的膨胀软件导致了主要的速度下降，PLC 系统未公开的 WiFi 密码阻止了控制器的更换。

作为一名 Android 开发者，[邻居]在他面前包围了围墙花园。这篇文章详细描述了在除了目标 x86 硬件之外的任何硬件上执行这种简单攻击的探索。

[![de-bloating app strips all non-essential software.](img/310ecabdf369d43f4070e2ae25146f11.png)](https://hackaday.com/wp-content/uploads/2021/09/samsung-plc-hack-debloat.jpg)

A debloating app strips all non-essential software.

(Neighborino)努力的第一个成果是针对老年平板电脑的黑客技术，它可以显示 WiFi 密码，允许用户将自己的控制器连接到智能家居。当然，这是黑客日，所以你知道[邻居]没有停止。

尽管不得不应对两种不同版本的 Android 和嵌入非黑客邻居公寓墙壁的平板电脑，[neighborhood ino]成功地从侧面装载了一台 APK。这让他们摆脱了安装原始系统的公司的束缚，并延长了斯诺登时代三星的寿命。一个去膨胀工具可以释放内存并将系统恢复到接近高性能的状态。一个重启调度程序使 x86 平板电脑在没有用户干预的情况下保持运行，当然，WiFi 密码揭示器使以前有围墙的花园变成了院子里的垃圾。

如果智能家居黑客是你的东西，我们最近报道了一个[语音控制智能家居设置](https://hackaday.com/2021/08/16/voice-controlled-smart-home-from-the-foundation-up/)，以及最近的另一个结合了[智能家居和哑终端](https://hackaday.com/2020/06/07/smart-home-meets-dumb-terminal/)。请务必通过[提示热线](https://hackaday.com/submit-a-tip/)与我们分享您自己的智能家居技巧！