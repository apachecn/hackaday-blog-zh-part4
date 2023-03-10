# 一种网络连接的 VFD 电子管时钟

> 原文：<https://hackaday.com/2020/02/06/a-network-attached-vfd-tube-clock/>

以太网供电(PoE)的优雅之处在于，您可以通过一根电缆提供网络连接和电源。不幸的是，似乎没有足够的硬件来支持这种能力，迫使勇敢的黑客自己动手。这一系列单线缆作品中最新的一款是[【Glen Akins】](https://bikerglen.com/blog/poe-vfd-tube-clock/)出品的这款漂亮的真空荧光显示(VFD)时钟。

[![](img/13180e88d707a6ea643aca9a4ace2850.png)](https://hackaday.com/wp-content/uploads/2020/02/poevfd_detail.jpg)

Testing the VFD tube socket

与谢妮的前辈相比，VFD 的一个关键优势是大大降低了能耗，在[Glen]计算了数据后，他发现使用六个 VFD 管的显示器可以轻松地通过标准 PoE 硬件供电。有了这些信息，他在 20 世纪 90 年代初开始设计 PCB，IV-12 管的优点是可以插接，因此如果需要，他可以很容易地将其拆除。

[Glen]首先必须为 IV-12 电子管创建一个原理图和 PCB 足迹，他可以导入到 Eagle 中，如果其他人正在使用这些特殊的电子管，他很乐意与大家分享。在新设计的插座测试成功后，他开始研究其余的电子产品。

该时钟由一个微芯片 PIC18F67J60 供电，该微芯片连接到以太网并从 NTP 下载当前时间。在看到这么多时钟使用 ESP 通过 WiFi 连接到互联网后，看到有线版本会有一些令人耳目一新的感觉。管段由 HV5812 驱动，也是微芯片品牌。最后，[Glen]使用了许多 DC/DC 转换器来产生驱动所有电子设备和 VFD 所需的 1.5 V、3.3 V、5 V 和 25 V 电压。

我们绝对喜欢这款钟的简洁，从它光滑的铝制外壳到背面的单个 RJ45 插孔。但是，如果你想找一个更闪亮的东西，[【Glen】也在假期里组装了一些 PoE 圣诞灯](https://hackaday.com/2019/12/31/poe-powers-christmas-lights-but-opens-up-so-much-more/)，它们与这个项目有许多共同的设计元素。

 [https://www.youtube.com/embed/RXZ56NHuO3g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RXZ56NHuO3g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢爱尔兰人的提示。]