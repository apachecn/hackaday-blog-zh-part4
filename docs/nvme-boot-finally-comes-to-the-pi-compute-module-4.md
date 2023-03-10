# NVMe 引导最后来到圆周率计算模块 4

> 原文：<https://hackaday.com/2021/03/29/nvme-boot-finally-comes-to-the-pi-compute-module-4/>

自从推出 Raspberry Pi 计算模块 4 以来，超级用户一直希望将 NVMe 驱动器与小巧的 ARM 板配合使用。虽然总是可以通过 IO 板上的适配器插入一个，但对于严肃的使用来说有点太笨拙了。[但是正如[Jeff Geerling]最近在他的博客](https://www.jeffgeerling.com/blog/2021/raspberry-pi-can-boot-nvme-ssds-now)上讨论的那样，我们不仅开始看到带有全尺寸 M.2 插槽的 CM4 载板，而且 Raspberry Pi 基金会已经公布了对从这些快速存储设备启动的测试支持。

[Jeff]看到的 MirkoPC 板本身当然令人印象深刻。即使你不喜欢跳过实际引导到 NVMe 的必要环节，你可以简单地插入一个标准驱动器并将其用于大容量存储的事实也是一个很大的优势。但是，该板还提供了几乎所有您可能希望从 CM4 获得的 I/O，甚至包括一些自己的细节，如 RTC 模块和带高质量耳机放大器的 I2S DAC。

一旦 NVMe 硬盘安全就位，并且你已经升级到测试版引导程序，你就可以和 SD 卡说再见了。但是现在还不要太兴奋。令人惊讶的是，[Jeff]发现从 NVMe 硬盘启动并不比 SD 卡快。也就是说，一旦系统启动并运行，实际上加载程序和其他日常任务要快得多。也许启动时间可以在未来的调整中得到改善，但老实说，目前启动 CM4 花费的 7 秒钟似乎并不过分。

[![](img/09e599afa418f7dc1bf31a0d1390cd95.png)](https://hackaday.com/wp-content/uploads/2021/03/cm4nvme_detail2.png)

[NVMe 硬盘是令人兴奋的技术](https://hackaday.com/2021/01/13/nvme-blurs-the-lines-between-memory-and-storage/)，很高兴看到更多的单板计算机支持它[。虽然它可能不会帮助您的 CM4 启动更快，但它肯定会全面提升性能，并扩展系统的功能。](https://hackaday.com/2020/12/22/new-part-day-hackboard-2-an-x86-single-board-computer/)

 [https://www.youtube.com/embed/4Womn10v71s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4Womn10v71s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

