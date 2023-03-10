# 以太网供电分离器提高谈判技巧

> 原文：<https://hackaday.com/2018/08/24/power-over-ethernet-splitter-improves-negotiating-skills/>

并非每个以太网设备都需要电源，这一事实使得 PoE 的实现变得很有趣；如果你开始给任何连接的设备供电，你会弄坏东西的。IEEE 802.3af 标准规定，能够提供电力的设备应该在协商电力水平之前检测接收电力的设备的存在。只有当这个过程完成时，电源设备才能提供其全部电源。当然，这需要智能的负担，这意味着有许多便宜的设备可以提供电力，而不管插入的是什么(被动 PoE)。

[Jason Gin]已经把一个旧的、便宜的无源 PoE 分离器升级到 802.3af 兼容(一个有源设备)。分离器被设计成与无源注入器配对，因此不能与 Jason 的有源 802.3at 基础设施一起工作。

![](img/549ef69ed15800b2c39deec246abd04e.png)

升级的大脑是 TI TPS2378 供电的设备控制器，它进行电源协商。它位于两个新电路板中的一个上，带有一个由一些太阳能电池 tab 线提供的基本散热器。第二块板包括电源接口，由双肖特基桥和一个 58 伏 TVS 二极管组成，用于处理电缆电感引起的任何电压尖峰。上图所示的以太网变压器是从一台废弃的 Macbook 上抢救下来的，经过一些搪瓷刮擦和精细的焊接，它适合使用。为了更深入地了解以太网变压器及其被黑的能力，[Jenny List] [写了一篇专门关注 Raspberry Pi 硬件的文章](https://hackaday.com/2018/06/01/raspberry-pis-power-over-ethernet-hardware-sparks-false-spying-hubub/)。

[Jason]的修改可以放入原来的盒子中，并且设备成功地与他的 802.3at 设置集成。我们喜欢[杰森]的作品，之前写过他在 eMMC 的冒险经历，[修理 windows 平板电脑](https://hackaday.com/2018/03/06/hot-air-surgery-revives-a-cheap-windows-tablet/)和[解释 SD 卡接口的复杂性](https://hackaday.com/2016/11/18/roll-your-own-64gb-sd-card-from-an-emmc-chip/)。