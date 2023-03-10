# 为 Adafruit Mini 热敏打印机编写自定义驱动程序

> 原文：<https://hackaday.com/2021/06/26/coding-a-custom-driver-for-the-adafruit-mini-thermal-printer/>

热敏打印机很酷……或者，呃，实际上很热。他们使用热量来制作图像，所以他们从来不需要墨水，他们在收据卷上打印。Adafruit 提供的热敏打印机是一个特别好的例子，因为它为初露头角的黑客提供了完整的文档。[Ed]就是这样一个人，他开始编写自己的驱动程序，以便在树莓 Pi 上使用 Linux 硬件。

这个项目是因为[Ed]不喜欢标准 Adafruit CUPS 驱动程序的半色调输出而产生的。因此，需要一个能够抖动的驱动器。该项目的第一步是通过在自定义驱动程序中运行这样的算法来实现抖动，以及改变打印头的加热时间来获得灰度能力。从那里，[这个驱动程序与 CUPS 集成在一起，并可以与 Linux lp 命令一起使用。](https://deathandthepenguinblog.wordpress.com/2019/12/31/adafruit-mini-thermal-printer-part-2-cups-and-other-vessels/)最后，[处理纸张用完的措施也被编码。](https://deathandthepenguinblog.wordpress.com/2019/12/31/adafruit-mini-thermal-printer-part-3-long-jobs-cancellation-and-paper-out/)

这是一次有趣的潜水，深入到与低级印刷商交谈的本质，这是我们在匆忙印刷音乐会门票时很少想到的事情。成功地打印一页纸需要做很多事情，而[Ed]的工作让我们更加尊重在纸上获得图像的所有事情。Github 上的热心修补者可以得到这个驱动程序。

同时，考虑热敏打印机来满足您所有的横幅打印需求。