# 冥王星(SDR)走向以太网

> 原文：<https://hackaday.com/2019/05/10/pluto-sdr-goes-ethernet/>

冥王星可能不再是一颗行星，但它仍然是一个由 ADI 公司设置的有趣的软件定义无线电(SDR)。这种廉价的收音机使用 USB 连接器，看起来有点像连接到 PC 的网络。但是如果你真的想用网络来使用它呢？[SignalsEverywhere] [向您展示如何使用 USB 网络适配器](https://www.youtube.com/watch?v=11_twp5VIwA)和 USB 连接适配器来完成此操作。

仅仅将 USB 加密狗插入盒子是不够的，还需要额外的电源以及少量的配置。IP 地址将是静态的，因此您可能想要使用 DHCP 服务器不会分配的 IP，或者在本地网络上保留该 IP。

Pluto SDR 是一个便宜的(150 美元)学生工具包，可以接收和发送(以非常低的功率)。也有一本关于它的免费书籍。默认情况下，该设备只能在 325 到 3800 MHz 范围内工作，例如，接收 FM 无线电波段太高。但是，有一个[黑客](https://wiki.analog.com/university/tools/pluto/users/customizing)不仅使范围从 70 到 6000 MHz，而且将带宽从 20 MHz 增加到 56 MHz。在增加的范围内，它可能不完全“符合规格”，但它可以很好地拾取调频信号。官方页面暗示这仅适用于特定的单位，但是我们知道有很多人可以让它工作，所以它可能也适用于你。

除了增加频率范围，您还可以[启用设备的第二个 CPU](https://www.reddit.com/r/RTLSDR/comments/7h2hh2/plutosdr_enable_2nd_cpu_core_for_better/) ，默认情况下该 CPU 是禁用的。如果你想做更多的黑客工作，有一个定制的固件可以把它变成一个独立的流媒体设备——方便的以太网黑客。你可以从 GitHub 下载 [PlutoWeb。](https://github.com/unixpunk/PlutoWeb)

 [https://www.youtube.com/embed/11_twp5VIwA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/11_twp5VIwA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

