# 微型开放硬件 Linux SBC 隐藏在众目睽睽之下

> 原文：<https://hackaday.com/2021/11/02/tiny-open-hardware-linux-sbc-hides-in-plain-sight/>

曾几何时，不太久以前，电脑是放在你桌子上的一个米色盒子。在此之前，电脑足够大，可以兼作桌子，甚至更远，它们占据了整个房间。今天吗？今天情况很复杂。像 Raspberry Pi 这样的单板计算机(SBC)将完整的桌面体验放在你的手掌上，其价格在智能手机革命增加对高性能 ARM 芯片的需求之前是不可思议的。

但是与 wifi watr 内部的[小型开放硬件 Linux SBC 相比，即使是树莓 Pi 看起来也很庞大。由[Walker]开发的作为渗透测试工具的定制计算机安装在一个外壳中，该外壳旨在使其看起来像传统的(如果有点大)USB 手机充电器。事实上，*不仅仅看起来*像 USB 充电器，它实际上就是一个。内部电源不仅能够将交流电转换为运行微型 Linux 盒子所需的各种 DC 电压，而且还具有一个 USB 端口，可以插入手机充电。](https://hackaday.io/project/179970-wifi-wart)

[![](img/31e21a7d8e90de6056e71b87e7e9ef6e.png)](https://hackaday.com/wp-content/uploads/2021/10/wwartprize_detail.jpg) 对于观众中的信息安全人士来说，无线电报的应用是显而易见的。只要把这个东西插在某个不显眼的地方，你就迈出了第一步。双 WiFi 接口意味着你可以在一张卡上连接到目标网络，并使用第二张卡来建立一个假的接入点或泄露数据。此外，凭借 1.2 GHz 的四核 Cortex-A7 ARM 处理器和健康的 1 GB DDR 3，您将有足够的能力在本地运行许多安全工具。

当然，没有什么可以阻止你将 WiFiWart 用于非安全目的。这让我们特别兴奋，因为你永远不会有足够的开放硬件 Linux 板。尤其是这么小的。除去墙上充电器的伪装，WiFiWart 的大脑可以用于各种项目。另外，不仅最终设计是开源的，而且 [[Walker]确保只使用免费和开源工具来创建它](https://machinehum.medium.com/i-put-a-wifi-router-into-a-phone-charger-final-post-c4be866e1d34)。保持他的整个工作流程开放意味着社区将更容易利用和改进他的初始设计，最终，这是开放硬件运动和努力(如 Hackaday Prize)背后的整个想法。

The [HackadayPrize2021](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)