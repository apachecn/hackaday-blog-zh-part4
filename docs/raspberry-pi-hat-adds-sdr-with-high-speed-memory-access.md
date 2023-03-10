# Raspberry Pi Hat 增加了 SDR 和高速内存访问

> 原文：<https://hackaday.com/2021/06/20/raspberry-pi-hat-adds-sdr-with-high-speed-memory-access/>

为 Raspberry Pi 添加 SDR 并不是一个新想法，但是开源的 cariboulite 项目看起来是进入这个领域的一个很好的开端。即使你对无线电不感兴趣，你也可能会对这个项目使用一个特殊的高带宽内存接口感兴趣。

有问题的接口是记录不良的 SMI 或二级存储器接口。[Caribou Labs]很有帮助地提供了其他人的链接，他们完成了解决接口的工作，还有[代码](https://github.com/jbentham/rpi)和[白皮书](https://github.com/cariboulabs/cariboulite/blob/main/docs/Secondary%20Memory%20Interface.pdf)。结果呢？根据 Pi 的不同，SDR 与处理器的数据交换速率最高可达 500 Mbps。特别提款权实际上用得比这少，大约 128 Mbps。尽管如此，使用传统方式传输这么多数据还是很困难的。

在无线电方面，SDR 覆盖 389.5 至 510 MHz 和 779 至 1，020 MHz。还有一个从 30 MHz 到 6 GHz 的宽调谐通道，但有一些例外。该板的发射频率约为 14 dBm，具体取决于频率，低频带的接收噪声系数低于 4.5 dB，3，500 MHz 以上的接收噪声系数低于 8 dB。当然，一些 Pis 已经有了一个[无线电](https://hackaday.com/2018/04/14/the-raspberry-pi-3b-as-an-sdr-without-the-sdr/)，但是没有这种能力。我们还看到 SMI 用于驱动[许多 led](https://hackaday.com/2020/10/12/running-way-more-led-strips-on-a-raspberry-pi-with-dma/)。