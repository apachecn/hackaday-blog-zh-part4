# Raspberry Pi 4 基准测试:处理器和网络性能使其成为真正的桌面竞争者

> 原文：<https://hackaday.com/2019/07/10/raspberry-pi-4-benchmarks-processor-and-network-performance-makes-it-a-real-desktop-contender/>

新的 [Raspberry Pi 4 发布了](https://hackaday.com/2019/06/23/raspberry-pi-4-just-released-faster-cpu-more-memory-dual-hdmi-ports/)，慢慢地，他们正在从微型中心和亚马逊分销网站走向世界各地的台式机和工作台。在你拿出一根新奇的 USB C 线并把它们插上之前，有必要了解一下你将会接触到什么。最新的树莓派卖得非常快。不仅如此，由于新的片上系统，它现在是一个可行的平台，用于廉价的自制 NAS、流媒体服务器或任何其他需要大量带宽的设备。这是未来的圆周率。

Raspberry Pi 4 采用了 BCM2711B0 片上系统，这是一款主频高达 1.5GHz 的四核 Cortex-A72 处理器，内存高达 4GB([暗示即将推出 8GB 版本](https://hackaday.com/2019/06/25/is-4gb-the-limit-for-the-raspberry-pi-4/))。Pi 的上一代产品 3 B+使用了 BCM2837B0 SoC，这是一款主频为 1.4GHz 的四核 Cortex-A53。与 3 B+相比，Pi 4 没有使用“高效”内核，我们凭借更大的高速缓存深入到了“性能”领域。但是这些数字在现实世界中意味着什么呢？这就是我们来这里的目的。

## Pi 4 是非常不同的硬件

树莓 Pi 和其他单板电脑的基准测试标准是[罗伊·隆巴顿的树莓 Pi 基准测试](http://roylongbottom.org.uk/Raspberry%20Pi%20Benchmarks.htm)。是的，你必须编译它们。当 Raspberry Pi 3 模型 B+发布时，我们可以忽略许多这些基准，因为内存芯片和 GPU 与 Raspberry Pi 2 相同；除了时钟速度之外，根本不会有什么有意义的区别，因为时钟速度本来就不太重要。这一次，不一样了。Pi 4 带来了全新的 SoC，新的 GPU，新的 RAM，以及新的一切。问题是，这重要吗？这些测试将比较树莓 Pi 4 型号 B+和树莓 Pi 3 型号 B+

## CPU 性能

LINPACK 测试简单地解决了线性方程，对于原始 CPU 性能来说是一个足够好的测试。该测试有两种形式，单精度和双精度。Linpack 性能指标评测的大幅提升是 SoC 变化的直接结果。Raspberry Pi 3 采用了四核 Cortex-A53，这是该系列中的“高效”内核。树莓 Pi 4 中的 Cortex-A72 具有更大的缓存[，Linpack 测量在一定程度上是对缓存大小的测量](http://roylongbottom.org.uk/Raspberry%20Pi%20Benchmarks.htm)。

[![](img/251a41d4a84506143e88c0185ce0aa3f.png)](https://hackaday.com/wp-content/uploads/2019/07/LINPACKh.png)

结果显示比树莓 Pi 3 有显著的增益。不过，这只是测试计算机的运算速度，系统的速度还远远不够。例如，内存带宽。

## 存储带宽

多年来，Pi 一直拥有 32 位内存总线，尽管这真的无关紧要，因为你只能得到 1GB 内存的 Raspberry Pi 3。几年前，RAM 被直接焊接到 SoC 上，这意味着当 RAM 芯片停止生产时，该型号的生产也将停止。RAM 一直是 Pi 的限制因素。随着圆周率 4 的出现，这种情况发生了变化。我们现在有一个 SoC，更多的数据和地址线连接到 RAM。哦，我们现在有超过 1GB 的内存。表现如何？

[![](img/490f883f1044c61e5f1776ac408d08b6.png)](https://hackaday.com/wp-content/uploads/2019/07/RAMspeedh.png)

Pi 4 显示了内存带宽的显著增加，但这是埋没了 lede。你现在可以得到一个 4GB 内存的 Pi，[8GB 版本已经在官方规格表中非正式地公布了](https://hackaday.com/2019/06/25/is-4gb-the-limit-for-the-raspberry-pi-4/)。如果让我猜的话，我会说我们可以在一年左右的时间里看到 8GB 的版本。至于内存带宽？谁在乎呢——我们现在有四倍的内存。

## 网络在有线和无线性能上远远超过 Pi 3

自 2012 年以来，Raspberry Pi 的架构一直存在一个问题，特别是流行的 B 型:USB 端口和以太网都挂在一个 USB 集线器上。从第一款 Raspberry Pi Model B 到上个月的 Raspberry Pi 3 Model B+，通过一个 [LAN7500 系列芯片](https://www.microchip.com/wwwproducts/en/LAN7500)控制 USB 口和以太网口。该芯片将单个 USB 连接(在 SoC 上)转变为几个 USB 端口和一个以太网控制器。虽然这是向片上系统添加端口的一个很好的部分，但有一个带宽限制:所有东西都必须通过 USB 2.0 连接，因此最大组合吞吐量将是 480 Mbps。无论 LAN7500 数据表中怎么说，千兆以太网都是不可能的，任何 USB 连接的使用都会消耗以太网的带宽。

好消息是，Raspberry Pi 4 中的新 SoC 具有以太网控制器:

[![](img/248da5a8f59bf45ede9a222eb8763454.png)](https://hackaday.com/wp-content/uploads/2019/07/PiEtherneht.png)

所有帐户的以太网连接都饱和了。这是一次从[speedtest.net](https://www.speedtest.net/)的 ping、下载和上传测试。我很幸运地拥有快速(且便宜)的光纤，而且从各方面来看，Raspberry Pi 4 正在以我的路由器所允许的最快速度传输数据。然而，Raspberry Pi 3 受到 USB 转以太网控制器的阻碍。树莓 Pi 4 现在是一个有能力的 4K 流盒，不仅仅是因为这是支持 4K HDMI 的树莓 Pi。

但是 WiFi 呢？树莓 3B+拥有板载 WiFi 和蓝牙，这要归功于一个 [CYW43455](http://www.cypress.com/documentation/product-overviews/cyw43455-wiced-ieee-80211ac-wifi-bluetooth-41-connectivity-solution) ，隐藏在印有树莓 Pi 标志的可爱射频屏蔽下的 Cypress 芯片组。树莓 Pi 4 失去了浮雕射频罐，但它的性能是否优于 3B+？

[![](img/3f6745aca197de6471f4aeb9f67bedbe.png)](https://hackaday.com/wp-content/uploads/2019/07/PiWiFih.png)

树莓 Pi 4 里的无线更好。虽然有线连接总是更好，但 Raspberry Pi 4 也毫不逊色，可以从房间另一端的路由器获得 85 Mbps 的速度。在相同的环境下，Raspberry Pi 3 只能处理 20 到 30 Mbps。

## 结论:反应灵敏，足以作为日常司机使用

Raspberry Pi 最初被设计为一台小型、廉价的 Linux 教育电脑，其理念是如果你给一个孩子一台电脑，他们就会学习 STEM，或者类似的东西。然而，计算机教育主要是潜移默化的；你不能告诉别人怎么编码，一定要有动手的时间。你不能教别人如何使用电子表格，你需要实践的时间。直到现在，Raspberry Pi 平台在功率和速度方面都落后于传统的台式机、笔记本电脑和 Chromebooks。这降低了 Pi 在教育中的影响。

现在，树莓派与任何桌面体验不相上下。如果树莓派 3 是一个有能力的电脑，当你需要快速查找一些东西时，它可以推到你的工作台下面，那么树莓派 4 就是一个有能力的日常司机。你完全可以用一台 Raspberry Pi 4 作为你的主电脑。它足够快，有足够的内存，网络很棒，它会做你想让它做的一切，响应速度和一千美元的台式机一样快。