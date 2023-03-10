# 冥王星频谱分析仪使用命令行

> 原文：<https://hackaday.com/2021/11/15/pluto-spectrum-analyzer-uses-command-line/>

如果你不关心短波频率，PlutoSDR 是一个很好的选择。该器件应该是 ADI 公司无线电芯片的评估板，但它作为软件定义无线电非常出色，可以接收和发送，甚至可以在内部运行 Linux。[SignalsEverywhere]展示了如何将它用作一个频谱分析仪，它可以在下面的视频中从命令行工作。

使用的软件是[逆行](https://github.com/r4d10n/retrogram-plutosdr)。尽管有 ASCII 图形，该程序有许多特点。您可以使用简单的按键来更改中心频率、采样速率、带宽等。您可以在 Linux 主机上运行该软件，或者在机器上编译二进制文件，或者使用 Raspberry Pi 上的工具进行交叉编译。

Pluto 通过 USB 连接，但看起来像一个网络适配器。这意味着你可以像远程计算机一样与它交谈，软件可以在主机上运行，也可以直接在装有 ARM 处理器的硬件上运行(如果你黑掉它的话，可以有[或两个](https://www.reddit.com/r/RTLSDR/comments/7h2hh2/plutosdr_enable_2nd_cpu_core_for_better/))。

我们在 GitHub 网站上注意到，像无处不在的 RTLSDR 加密狗这样的通用设备支持计划正在进行中。我们很乐意看到有人接手这项工作。还有鼠标调整、瀑布显示和 HTML 输出的计划。

在之前，我们已经讨论过[冥王星。我们还看到[SignalsEverywhere]报道了](https://hackaday.com/2020/04/14/pluto-might-not-be-a-planet-but-it-is-an-sdr-transceiver/)[如何连接冥王星以太网](https://hackaday.com/2019/05/10/pluto-sdr-goes-ethernet/)。

 [https://www.youtube.com/embed/2dJGL1rBlIo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2dJGL1rBlIo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

