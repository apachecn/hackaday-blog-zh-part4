# 这个树莓派迷你 ITX 板有大量的 IO

> 原文：<https://hackaday.com/2021/11/28/this-raspberry-pi-mini-itx-board-has-tons-of-io/>

树莓派现在有各种各样的版本。有微小的零，当然还有主流尺寸的主板。然后，有最新的最大的计算模块 4，准备好插槽到载板，以爆发其所有的 IO。Seaberry 就是这样一种设计，正如[Jeff Geerling]所展示的，它为 CM4 提供了一个迷你 ITX 外形和一吨 IO。(视频中断后嵌入。)

Seaberry 拥有一个全尺寸 x16 PCI-E 端口，带宽仅为 1 倍，但能够容纳全尺寸的卡。顶部还有四个 mini-PCI-E 插槽，下面隐藏着四个 M.2 E-key 插槽。然后，主板的中间有一个 M.2 插槽用于 NVME 驱动器，x1 PCI-E 插槽悬挂在侧面。

端口包括一个 USB 2.0、一个 Cisco 风格的串行控制台端口、两个 HDMI 端口和一个千兆以太网插孔。提供两个独立的 12V 连接器，允许冗余电源设置，通过添加正确的以太网供电硬件，可以实现三重冗余。当然，Seaberry 还具有常见的 40 引脚 GPIO 接头、14 引脚 CM4 IO 接头以及常见的 DSI、CSI 和 RTC 连接。

迷你 ITX 的设计是一个特别的恩惠。Seaberry 可以很容易地放入一个迷你电脑机箱中，电源按钮和活动 led 就像你预期的那样工作。

在测试主板时，[Jeff Geerling]几乎填满了每个插槽，试图看看在 8GB RAM 的计算模块 4 上可以运行多少张卡。在 NVME SSD 驱动器，几个用于机器学习的 Coral TPUs，多个网卡和一个 SATA 接口方面没有问题。

由于驱动程序的限制，并不是所有的东西都能工作，但是总线上列举的所有东西都很好。[杰夫]早期的工作在这里得到了回报。他之前试图让 GPU 在平台上工作的尝试意味着为 PCI 设备开辟一个扩展的 BAR 空间不成问题。

进一步的尝试包括添加一个 12 卡托架，装载 7 个以上的 TPU、5 个以上的 WiFi 卡和 3 个以上的 NVME 驱动器。除了过量 NVME 驱动器导致的一些内核崩溃之外，Pi CM4 仍然能够检测到一切，表明它可以处理 20 多个 PCI-E 设备而不会出现重大问题。

向 Pi CM4 扔这么多设备可能在主流中没有明显的应用，但它肯定会被证明对某人有用。我们当然很喜欢看[Jeff]推动 CM4 的极限，我们希望他尽快让 GPU 工作起来。

 [https://www.youtube.com/embed/6dzSFUt6C6U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6dzSFUt6C6U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

