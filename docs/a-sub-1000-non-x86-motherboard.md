# 低于 1000 美元的非 X86 主板

> 原文：<https://hackaday.com/2018/11/26/a-sub-1000-non-x86-motherboard/>

如果你正在建造一台计算机，你的选择几乎是无限的。你可以得到一个带有红色发光二极管、蓝色发光二极管、绿色发光二极管的主板，或者如果你觉得贵的话， *RGB 发光二极管*。你可以得到定制的任何形状的散热器，只要它是有棱角的，能让你尖叫。如果你想要一个不使用 x86 的主板——无论是 AMD 还是 Intel——你就有点不走运了。要么不存在，要么要花一笔小钱。

Raptor Engineering 刚刚发布了一款不是 x86 的主板，价格也不像廉价汽车那么贵。黑鸟主板是为 IBM Power9 CPU 设计的，价格仅为 800 美元。再加上[一个四核 CPU](https://secure.raptorcs.com/content/CP9M01/intro.html) ，总成本约为 1200 美元。加上一些 ECC 内存，你仍然低于 2000。使用非 x86 CPU 构建从未如此便宜。这与来自[Raptor Engineering 的早期版本相比是一个显著的变化，在早期版本中，仅主板](https://hackaday.com/2016/09/19/new-part-day-a-truly-secure-workstation/)就花费了 3700 美元。

Blackbird 主板具有两个 DDR4 ECC DIMM 插槽、一个 PCI Express 4.0 x16 插槽、一个 PCI Express 4.0 x8 插槽、两个千兆以太网端口、4 个 SATA 3.0 端口、4 个 USB 3.0 端口、1 个 USB 2.0 端口和一个 HDMI 显示输出。

你建造一台基于 Power9 的计算机的唯一原因只是为了避开已经成为英特尔和 AMD CPUs 的黑匣子。没有人真正知道英特尔管理引擎中发生了什么，AMD 也有类似的黑匣子。然而，使用 Power9 CPU 有一个安全的引导模式，如果你的计算机在物理上是安全的，你或多或少可以确信你正在运行你的固件、内核和用户空间应用。这是为有安全意识的人准备的安全。RISC 架构将改变一切。