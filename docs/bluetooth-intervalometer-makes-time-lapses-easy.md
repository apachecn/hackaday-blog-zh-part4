# 蓝牙间隔计让时间流逝变得容易

> 原文：<https://hackaday.com/2020/02/21/bluetooth-intervalometer-makes-time-lapses-easy/>

拍摄时间流逝是许多摄影师的一种有趣的消遣。虽然大多数现代相机都有一些功能来实现这一点，但如果你真的想进入其中，你会想要一个间歇时间表来运行这个节目。为了实现这一目标，[扎克]决定不购买现成的产品，而是自己动手制作。

该版本依靠 Arduino Nano 来运行该节目，结合流行的 [HC-05 蓝牙模块。](https://www.amazon.com/dp/B071YJG8DR/)蓝牙模块允许设备与[Zach]使用 RoboRemo 创建的智能手机应用程序进行通信。这是一个让初学者轻松创建定制 USB、WiFI 和蓝牙应用的平台。该应用程序向 intervalometer 发送关于拍摄照片数量以及每次拍摄之间等待时间的指令。然后，它触发延时，Arduino 通过短路插入相机的 TRS 插头上的相关引脚来触发相机。

这是一个简单的构建，大多数黑客可能用垃圾箱中的部分来完成。此外，构建您自己的产品提供了完全根据您的需求进行定制的可能性。当然，你可以避开现代，而是机械地做事。休息后的视频。

 [https://www.youtube.com/embed/_kHvHdEXhos?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_kHvHdEXhos?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

