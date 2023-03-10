# Raspberry Pi 通过 GPIO 头获得 PATA/IDE 驱动器

> 原文：<https://hackaday.com/2020/08/10/raspberry-pi-gets-pata-ide-drive-via-gpio-header/>

总的来说，Raspberry Pi 是一款避开传统界面的电脑。主要依靠 SD 卡进行存储和 USB 端口进行进一步扩展，磁性硬盘很少见。然而，[Manawyrm]认为 40 针是合适的，[并着手为该平台制作 PATA IDE 适配器。](https://github.com/manawyrm/pata-gpio)

为了实现现在老式的 IDE 设备与 Raspberry Pi 的接口任务，[Manawyrm]选择使用单板计算机的 GPIO 引脚来完成这项工作。需要 23 个引脚，其中 16 个用于数据总线，其余专用于地址线、选通脉冲和其它功能。

该适配器不是速度恶魔，在 Raspberry Pi 4 中读取速度为 800 KiB/秒，写入速度为 500 KiB/秒。主要的瓶颈来自于对 libgpiod 的依赖,[Manawyrm]欣然承认它是为一般的 IO 任务而设计的，而不是数据传输。尽管如此，它仍然足够快，可以从 IDE CD-ROM 驱动器上播放音频 CD 而不会跳过。然而，内核构建是必需的，因为不出所料，默认情况下，Raspberry Pis 没有配置为使用 ATA 磁盘。

显然，更严肃的应用程序会用专用的 USB 硬盘适配器[或给 Raspberry Pi 一个 PCI-express (PCIe)卡](https://hackaday.com/2020/07/01/adding-pcie-to-your-raspberry-pi-4-the-easier-way/)来代替 sata 驱动器，但这并不影响构建中固有的乐趣。虽然它可能很慢，但它表明，当您了解基本知识时，与 PATA 硬盘对话实际上是非常简单的。当然，如果你想反其道而行之，[，让你的树莓派模仿 PATA 磁盘，这也是可能的](https://hackaday.com/2017/04/12/hackaday-prize-entry-real-hard-drives-in-the-raspberry-pi/)。休息后的视频。

 [https://www.youtube.com/embed/cHQhuzSn2oE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cHQhuzSn2oE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 DosFox 的提示！]