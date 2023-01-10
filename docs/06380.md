# GPU 变成无线电发射器，打败空气隙个人电脑

> 原文：<https://hackaday.com/2020/04/24/gpu-turned-into-radio-transmitter-to-defeat-air-gapped-pc/>

又是一周，针对空气隙计算机的又一次利用。而这一次的攻击尤为巧妙和恶毒:[将 GPU 变成无线电发射器](https://duo.com/labs/research/finding-radio-sidechannels)。

[Mikhail Davidov]和[Baron Oldenburg]文章的第一部分回顾了使用软件定义无线电(SDR)加密狗探索计算机射频辐射的一些基础知识。大多数读者可以放心地稍微向前跳到第 9 节，进入他们用来嗅探来自气隙测试计算机的潜在危害 RF 泄漏的过程。在发现几个千兆赫范围内的微弱信号并因其有限的渗透潜力而将其作为攻击媒介排除后，他们决定采用镭龙 Pro WX3100 的 GPU 卡，特别是其 ATI 芯片组的电源管理功能。

随着 GPU 基准测试程序的运行，他们在两个最低功耗设置之间切换显卡着色器时钟，从而在 SDR 瀑布上产生了 428 MHz 的强信号。他们能够在 50 英尺(15 米)远的地方接收到这一信号，这可能会让附近的火腿们感到烦恼，因为这是在 70 厘米波段的中间位置。理论上，这足以过滤数据，但比特率非常低。因此，他们通过强制 CPU 驱动程序以 1 兆赫的步长改变着色器时钟频率来改进这种利用，从而允许他们实现更高吞吐量的编码方案。您可以在下面的视频中听到由不同图形显示引起的信号变化；人们不需要太多的想象力就能看出恶意软件如何利用这一点来渗透计算机上的几乎任何东西。

这是一次令人着迷的黑客攻击，向[达维多夫]和[奥尔登堡]致敬，他们揭露了这一弱点。我们将不得不把这一点与 Samy Kamkar 在 2019 年 super co talk 中提到的所有其他[旁门左道攻击放在一起。](https://hackaday.com/2020/03/09/fear-of-potato-chips-samy-kamkars-side-channel-attack-roundup/)

 [https://www.youtube.com/embed/-RXo0wIZ2ao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-RXo0wIZ2ao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过[汤姆的硬件](https://www.tomshardware.com/news/amd-radeon-gpu-steal-data-graphics-cybersecurity)