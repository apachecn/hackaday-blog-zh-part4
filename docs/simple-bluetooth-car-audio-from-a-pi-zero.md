# 来自 Pi Zero 的简单蓝牙汽车音频

> 原文：<https://hackaday.com/2019/08/13/simple-bluetooth-car-audio-from-a-pi-zero/>

当[Sami pietik inen]意识到他汽车内置的蓝牙不支持音频时，他没有扔掉它，而是买了一辆特斯拉。相反，他决定通过建造一个插入辅助插座的[小型蓝牙设备来解决这个问题。为此，他使用了一个带有](https://pagefault.blog/2019/07/31/building-a-bluetooth-dac-with-raspberry-pi-zero-w/) [pHAT DAC](https://shop.pimoroni.com/products/phat-dac) (数字音频转换器)的 Raspberry Pi Zero。这也许是用大锤敲碎核桃，但有时你会利用你所拥有的。有趣的部分在于他接下来做了什么:他使用 Yocto 优化设备，使其尽可能简单明了。

这是因为他在第一版中使用的 Raspbian 操作系统做的比需要的多得多:该设备只需处理蓝牙和音频输出，并不需要 Raspbian 试图安装和运行的所有其他东西。

所以在第二个版本中，他放弃了 Raspbian，使用了 [Yocto](https://www.yoctoproject.org/) ，这是一个允许你创建定制的 Linux 发行版的项目。通过剔除项目不需要的东西，他使项目更快更精简。他使用了 [Meta-raspberrypi](http://git.yoctoproject.org/cgit.cgi/meta-raspberrypi) ，这是一个板支持包(BSP)，为在 pi 上运行 Yocto 提供了基础，然后调整了一个预建的 Yocto 映像，禁用了所有他不需要的功能。

结果是一个更简单的设备，它可以在大约五秒钟内启动并准备好播放音乐。与标准 Raspbian 映像 30 到 60 秒的启动时间相比，这是一个相当大的改进(假设它能够启动)，并且是一个很好的例子，说明有时越简单越好。