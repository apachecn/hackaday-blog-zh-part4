# ZRAM 提高了树莓派的性能

> 原文：<https://hackaday.com/2020/05/20/zram-boosts-raspberry-pi-performance/>

Linux 是一把双刃剑。一方面，您可以配置太多东西。另一方面，您可以配置太多东西。有时很难知道应该做什么才能获得最佳性能，尤其是在像 Raspberry Pi 这样的小平台上。[Hayden James]有一个建议:启用 [ZRAM](https://haydenjames.io/raspberry-pi-performance-add-zram-kernel-parameters/) 并调整内核来匹配。

虽然这篇文章关注的是 Raspberry Pi 4，但它适用于任何内存有限的 Linux 系统，包括旧的 Pi 板。这个想法是使用一部分主存作为交换文件。起初，这似乎是一种浪费，因为你可以用这些内存来运行程序。但是，交换设备是压缩的，因此您可以获得更多的交换空间，与硬盘或固态硬盘相比，从这些压缩的交换设备和主内存进行传输的速度非常快。

除了打开基于 RAM 的交换之外，重要的是调整内核以更多地利用交换，因为交换速度相对较快。建议的设置会更改以下系统参数:

*   `vm.vfs_cache_pressure`–增加清除文件缓存的频率，以释放更多内存。
*   `vm.swappiness`–让内核更有可能使用 swap。请注意，ZRAM 交换比较慢的交换文件具有更高的优先级。
*   `vm.dirty_background_ratio`–在写入交换区之前，允许指定数量的内存页面变脏。
*   `vm.dirty_ratio`–在 I/O 开始阻塞之前对脏页的绝对限制，直到脏页被写完。

当然，这些参数对您的设置来说可能是最好的，也可能不是，所以您可能想尝试一下。如果你想了解更多关于你有多少脏页的信息，看看里面的内容。

这就是 Linux 的好处。你可以改变事情，看看发生了什么，如果你喜欢，再改变一次。如果你想用 htop 更深入地了解你的系统的操作，你会想要[仔细阅读那个程序](https://hackaday.com/2020/01/30/understand-linux-htop-visually/)。这种技术正是那些小型的 [Linux 系统](https://hackaday.com/2018/11/12/new-part-day-a-6-linux-computer-you-might-be-able-to-write-code-for/)所需要的。