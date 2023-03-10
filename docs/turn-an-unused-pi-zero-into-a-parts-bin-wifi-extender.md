# 将未使用的 Pi Zero 变成零件箱 WiFi 扩展器

> 原文：<https://hackaday.com/2020/05/10/turn-an-unused-pi-zero-into-a-parts-bin-wifi-extender/>

我们知道你们很多人都坐在一个没有用过的树莓派 Zero W 上，甚至可能有几个。这些东西太小太便宜了，所以当机会出现时，不能不大量购买。不幸的是，Zero 并不完全是一个发电站，有时很难找到一个真正适合硬件的应用程序。

这就是为什么这篇来自[Tejas Lotlikar]的技巧值得一看。使用 Pi Zero W，一个便宜的 USB WiFi 适配器，和一些软件诡计，[你可以为你的无线网络组装一个便宜的扩展器](https://hackaday.io/project/171296-truly-wifi-extender)。Pi 甚至应该有几个周期来运行像 Pi-hole 这样的广告拦截软件，同时在管道周围洗牌。

[Tejas]解释了该过程的每一步，从将 Raspbian 图像放入 SD 卡，到说服`wpa_supplicant`将 Pi 的 WiFi 无线电设置为接入点模式。顺便说一句，这意味着您不需要对 USB 无线适配器的品牌和型号非常挑剔。最好使用外置天线，因为它能够接收微弱的源信号，但你不必担心它支持软 AP。

配置好软件后，你只需要一个附件就可以完成这个项目。[一个定制的 3D 打印外壳足够大](https://hackaday.com/2018/03/02/printed-it-custom-enclosure-generator/)以容纳 Pi 和外部 WiFi 适配器将是一个不错的选择。