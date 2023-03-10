# RoboTray 是一个秘密茶管家

> 原文：<https://hackaday.com/2021/09/17/robotray-is-a-secret-tea-butler/>

为了喝杯茶，你会走多远？[samsungite]的妻子不喜欢她的工作台面上杂乱无章，所以单杯水壶会放回橱柜，以便下次泡茶时使用。只要那里有空间，为什么不把它永久地安装在那里呢？这就是 robot ray(T1)背后的想法，如果能够以某种方式进行探测，它只会更酷。

RoboTray 经历了几次迭代，最重要的是从 6mm 的 MDF 转换到 4 mm 的铝板。变压器充当电流传感器，当水壶通电时，托盘首先使用 12 VDC 电机和 Arduino 向前移动 7 厘米。然后，它在由另一台 12 伏直流电机驱动的转盘上旋转 90 度。水壶足够智能，可以在完成后自动关闭，Arduino 可以感知到这一点，并在 10 秒钟的警告期后逆转所有步骤。休息之后，请查看实际情况。

如果[samsungite]还有更多 Arduinos，他可能会喜欢这个[茶叶库存跟踪器](https://hackaday.com/2019/02/20/a-modern-solution-to-tea-bag-inventory-management/)。

 [https://www.youtube.com/embed/lNIFaGxzayg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lNIFaGxzayg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

