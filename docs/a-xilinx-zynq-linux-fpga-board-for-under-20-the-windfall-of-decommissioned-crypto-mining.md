# 售价不到 20 美元的 Xilinx Zynq Linux FPGA 板？退役地下采矿的意外收获

> 原文：<https://hackaday.com/2020/12/10/a-xilinx-zynq-linux-fpga-board-for-under-20-the-windfall-of-decommissioned-crypto-mining/>

硬件可用性的一个令人兴奋的趋势是 FPGA 板和模块不可阻挡地朝着价格低廉的方向发展。曾经令人眼红的价格现在只是一个昂贵的价格，毫无疑问，在未来几年将成为一种商品。尽管在市场底部仍然存在价格差距，所以在全球速卖通上发现低于 20 美元的 Xilinx Zynq 主板，在同一芯片上结合支持 Linux 的 ARM 内核和 FPGA，肯定是一件非常有趣的事情。我的一个 hackerspace 社区朋友订购了一个，昨天它以通常的匿名包裹从中国到达。

## 有一个陷阱，但只是一个小陷阱

[![The heftier of the two boards, in all its glory.](img/f2be100a728b06a6bf8276272d580228.png)](https://hackaday.com/wp-content/uploads/2020/11/antminer-fpga-board-full.jpg)

The heftier of the two boards, in all its glory.

有两种主板待售，一种采用 Zynq 7000，另一种采用 7010，Xilinx 产品选择器告诉我们这两种主板都采用了相同的 ARM Cortex A9 内核和 Artix-7 FPGA 技术。7000 包括一个具有 23k 逻辑单元的单核，7010 上有一个具有 28k 逻辑单元的双核。我朋友点的是后者。

好消息来了，但其中肯定有猫腻，对吧？没错，但这不是不可逾越的障碍。这些不是新产品，而是老一代 AntMiner 加密货币采矿钻机的控制板。这些组件有 2017 年的日期代码，所以它们在过去三年里一直连接到某个采矿数据中心的一对 ASIC 或 GPU 板。加密货币技术不断变化的步伐意味着它们现在是多余的，我们是过剩市场的幸运受益者。

## 获得 Linux Shell 就是这么简单！

[![Linux, in minutes!](img/3613fe066bfec9fbbb1703d3e126e5e7.png)](https://hackaday.com/wp-content/uploads/2020/11/antminer-fpga-board-linuxl.jpg)

Linux, in minutes!

在 PCB 上是一个巨大的 BGA 中的 Zynq 芯片，其 I/O 线引出到一排用于矿工板的插座、以太网、SD 卡插槽、几个 led 和按钮以及 ATX 12V 电源插座。串行和 JTAG 端口很容易识别和访问，将 USB 转串行适配器连接到前者会将我们带到 Linux 登录提示符下。一个小小的引导装载程序外壳魔术允许密码被重置，我们有了一个可用的外壳。改变跳线允许从 SD 卡启动，因此将您自己的 ARM Linux 版本带到设备上以取代 AntMiner 版本是非常简单的，并且由于 Zynq 可以从 Linux 内加载其 FPGA 代码，这使得价格非常容易获得 FPGA 开发板。

这些电路板似乎是由多家供应商提供的，这表明供应链中肯定有不少供应商。股票不可避免地会售完，所以如果你没有买到，也不要绝望。相反，它们表明了专用 FPGA 板被我们的社区重新设计为通用开发板的增长趋势(例如[我们在 1 月份介绍的可拆卸 LED 驱动板](https://hackaday.com/2020/01/24/new-part-day-led-driver-is-fpga-dev-board-in-disguise/)中的点阵 FPGA)。随着他们这一代 FPGA 技术开始被取代，他们肯定会被其他人加入。

我们会密切关注任何其他人，我们确信如果你看到任何人，你会给我们小费。