# 用 Onion Omega2 Pro 改进基于路由器的开发板

> 原文：<https://hackaday.com/2018/12/27/improving-router-based-dev-boards-with-the-onion-omega2-pro/>

在我们有 Raspberry Pis 和 Beaglebones 之前，将 Linux 系统放入小型可移植项目的艺术仅限于路由器黑客。古老的 WRT54G 通过精心应用 Unix-ey 固件来控制联网机器人。现在，情况不同了，但是仍然需要一个便宜的、可移植的、足够好的 Linux 系统来完成这项工作。现在，继路由器黑客[之后，又有一款升级版的主板上市](https://www.crowdsupply.com/onion/omega2-pro)，洋葱 Omega2 Pro 上市了，它有更多的按钮，更多的开关，但仍然比试验板小。

Onion Omega2 Pro 是几年前推出的支持试验板的 SoM 的升级版。专业版采用 580 MHz MIPS CPU，512 MB 内存(更新:这是 128 MB 物理内存和 384 MB 闪存交换文件)，8 GB 存储空间，以及与 b/g/n WiFi 的连接。与以前的版本不同，这是一个功能更强大的系统，具有 30 针扩展接头，支持电池充电，用于充电和串行的微型 USB，以及 USB 主机端口。因为它的核心是开发板上的路由器，所以您还可以享受 WiFi 网络的所有乐趣。扩展接头连接到各种附加设备，包括 GPS 模块、有机发光二极管显示器和以太网端口。

现在我们有 Raspberry Pis 和其他各种基于片上智能手机系统的电路板，但有时你不需要那么多开销。你不需要怪异的 Linux 发行版来处理 ARM 引导加载程序。有时候你只需要一些简单的东西，洋葱 Omega2 Pro 就是这么做的。