# 解剖 T1 线路

> 原文：<https://hackaday.com/2022/06/01/dissecting-a-t1-line/>

当谈到互联网连接时，在 2022 年，我们中的许多人都很容易。我们的 ISP 为我们提供光纤、电缆或 DSL 线路，我们只需插上电源就可以使用。它变得无处不在，以至于许多客户不再使用模拟电话线，而模拟电话线往往是套餐的一部分。但是在 DSL 接入变得容易之前，有租用线路，这是[老 VCR]正在剖析的其中之一。问题中的线路是 1.536 Mbit/s 的 T1 连接，在他的有线电视提供商提供可靠服务之前，安装成本很高，但十多年后，现在已经过剩。ISP 没有要回他们的路由器，那么除了给它黑客待遇还能做什么呢？

在一篇冗长的博客文章中，他带我们详细了解了什么是 T1 线路，以及如何使用两根铜线安装 T1 线路，然后才开始讨论路由器本身。这是一款过时的三星设备，当他检查芯片时，他发现不是我们期待的那个时期国产设备的 MIPS 或 ARM 处理器，而是飞思卡尔的 PowerPC SoC。连接到串行端口显示它从 SD 卡运行 SNOS 或三星网络操作系统，一些实验通过 bootloader 命令找到了默认的密码重置程序。这篇文章的其余部分致力于探索这个操作系统。

在 Raspberry Pi 和类似的廉价 Linux 主板出现之前，黑客入侵路由器是获得廉价嵌入式 Linux 系统的一种方式，但现在要将路由器从制造商和电信公司的魔掌中解放出来，还需要做更多的工作。尽管如此，这仍然是 Hackaday 常见的一部分。