# 使用未记录的 API 控制 M1 MAC 电脑上的外部显示器

> 原文：<https://hackaday.com/2021/09/08/controlling-external-monitors-on-m1-macs-with-undocumented-apis/>

显示数据通道(DDC)是现代数字显示器的一项非常有用的功能，因为它允许显卡(以及操作系统)与显示器通信，并控制亮度和对比度等功能。这里最大的负面影响是在像 MacOS 这样的操作系统中很难使用这一功能，这可能会因一时兴起而改变，正如[阿林·帕奈提乌]最近发现的那样。

当前显示器实现 [DDC2](https://en.wikipedia.org/wiki/Display_Data_Channel) ，它是基于一个 I ² C 总线。尽管如此，很少有操作系统提供基于 DDC 的功能控制，如亮度，这就是[阿林]为 MacOS 开发的一个受欢迎的实用程序，它使用未记录的 API 通过 I2C 与外部显示器对话 DDC2。直到新的基于 Arm 的 Mac 系统发布，这些未记录的 API 被修改。

尽管有一些方法可以解决这个问题，一些实用程序使用简单的基于软件的覆盖来“调暗”显示器，或者通过连接到 HDMI 的外部 Raspberry Pi 系统使用外部伽马调节，并使用 [ddcutil](https://github.com/rockowitz/ddcutil) ，但最好的方法仍然是通过 DDC2。最终发现了提供访问的新的(未记录的)API，另一个名为[卓伟]的用户通知[阿林]基于 Arm 的 MacOS 的新的`IOAVServiceReadI2C`和`IOAVServiceWriteI2C`方法。

在这之后，在有多个外部显示器的情况下，需要更多的调查才能确定 I2C 总线上的哪些设备是哪个显示器，但最终它又工作了，将基于硬件的亮度控制重新放回到 MacOS 用户手中。除了 M1 Mac Mini 上的 HDMI 和一些显示器的一些明显的硬件问题，但谁会去计算呢？

【标题图片:MacOS 上的 Lunar app 截图。鸣谢:阿林·帕奈提乌]