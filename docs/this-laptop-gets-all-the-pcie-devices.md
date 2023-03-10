# 这台笔记本电脑拥有所有的 PCIe 设备

> 原文：<https://hackaday.com/2022/04/20/this-laptop-gets-all-the-pcie-devices/>

您是否曾经觉得您的笔记本电脑的 GPU 不是最佳的，或者您的笔记本电脑可以使用 SAS 控制器？[Rob Rogers]也有这种感觉，所以现在他有了唯一一台配有 AMD rx 580 GPU 的 Dell Latitude 企业级笔记本电脑，还有更多。由于他从 WiFi 卡上劫持了一个 PCIe 链接，他成功地获得了一个 SAS 控制器，一个 USB 3.0 扩展卡，前述的 GPU 和一个双端口服务器网络适配器，所有这些都在一个单一的桌面设置中，如视频所示。

首先，我们看到一个基于 PLX 制造的芯片的 PCIe 分组交换板，用蓝色胶带包裹着，把一条 PCIe x1 链路分成八条。传统的 USB 3.0 电缆将下游的 x1 链路传送到四个相连的 PCIe 卡，所有这些都放在[Rob]的桌子上。[Rob]演示了所有卡的功能是否正常 SAS 控制器连接到存储容量为 22 TB 的服务器背板，一些设备插入 USB 3.0 卡，以太网电缆与网卡中的活动链接，并结束了显示 RX580 与笔记本电脑移动 CPU 清晰配对的 3DMark 结果的视频。PCIe 开关卡上还有四个点，所以如果你想连接几个 NVMe 固态硬盘，而不需要通常需要的昂贵的 USB 外壳，你绝对可以！

现在，我们没有看到更多这样的黑客攻击是有原因的。这似乎是一个 Latitude E5440，卡插入到一个迷你 PCIe 插槽中，这意味着整个装置由一个 PCI-E Gen2 x1 链接绑定，这大大抵消了你在玩游戏时从外部 GPU 获得的收益。然而，当谈到外设的类型和数量时，这是无与伦比的-如果你想在你通常随身携带的同一台计算机上添加外部 GPU、高速网络和 SAS 控制器，实际上没有一个坞站可供你购买！

我们收集的酷 PCIe 黑客一直在增加，黑客们[通过 ExpressCard](https://hackaday.com/2011/10/19/beefing-up-your-laptops-gaming-chops-with-an-external-gpu/) 和[迷你 PCIe](https://hackaday.com/2015/03/26/a-laptop-with-an-external-graphics-card/) 添加外部 GPU，[在工厂拒绝提供的地方安装 PCIe 插槽](https://hackaday.com/2011/03/15/no-pcieslot-just-add-one/)，以及[扩展板载 M.2 插槽](https://hackaday.com/2017/04/17/broken-yoga-becomes-firewall/)用于全尺寸 PCIe 卡。如今，有了这些分组交换机，为任何支持 PCIe 的设备配备一系列功能都变得很容易——正如这款带有【T11 个 PCIe 插槽的 Raspberry Pi 计算机模块[主板所示。想知道 PCIe 是如何运作的，为什么所有这些都是可能的？我们已经就此写了一整篇文章。](https://hackaday.com/2021/11/28/this-raspberry-pi-mini-itx-board-has-tons-of-io/)

 [https://www.youtube.com/embed/jM0PHdFrYLY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jM0PHdFrYLY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

