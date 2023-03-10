# 不太 USB-C 的任天堂 Switch 配件

> 原文：<https://hackaday.com/2019/08/04/the-not-quite-usb-c-of-nintendo-switch-accessories/>

从历史上看，游戏机的销售利润很低甚至为零，目的是以较低的前期价格吸引消费者。真正的利润来自游戏和配件的销售。为了从后者中分一杯羹，售后配件制造商以不同的“兼容性”水平推出逆向工程兼容产品。

当任天堂 Switch 推出带有标准 USB-C 端口的配件时，我们曾希望那种漫无目的的逆向工程时代已经结束，但现实并非如此。Redditor [VECTORDRIVER]总结了这个故事的几个部分，其中[任天堂偏离了规范，配件制造商仍然出错](https://www.reddit.com/r/NintendoSwitch/comments/ckaiiv/an_engineers_pov_on_the_3rd_party_dock_switch/)。

官方上，任天堂[宣布该开关符合 USB-C 标准](https://www.nintendo.com/switch/tech-specs/)。但是正如我们最近报道的，USB-C 是[一只庞大而复杂的野兽](https://hackaday.com/2019/07/29/usb-c-one-plug-to-connect-them-all-and-in-confusion-bind-them/)。决心找到问题的根源，困惑的消费者在互联网上联合起来收集轶事证据并进行推测。一种说法是，任天堂的官方 dock 为了追求特定的触感，偏离了官方的 USB-C 尺寸；即减少 USB-C 引脚正确对齐的公差和使用内部机制进行补偿的[。由于任天堂在规格上反复无常，这使得开发正常运行的售后配件变得更加困难。](https://www.reddit.com/r/NintendoSwitch/comments/5qoguz/inside_of_the_nintendo_switch_dock/)

但这并不是一家公司在售后市场出现失误的唯一方式。一次拆解显示，Nyko 没有使用专用芯片来管理 USB 电源传输，而是选择在 ATmega8 上运行的软件中实现它。我们可以推测一下为什么(零件成本？上市时间？)但更重要的是，我们可以读取其输出引脚上过高的实际电压。每一次使用都变成了一场危险的游戏，比如“今天这个开关能承受高于规格的电压吗？”我们预计，随着 USB-C 变得越来越普遍，使用专用芯片将很快变得最便宜、最容易，消除了独立实现的工作和出错的风险。

对于一项新的复杂技术来说，在它们走向普及的道路上，这些都是相当典型的初期问题。早期 USB 键盘和鼠标并不总是有效，早期 PCI-Express 卡和主板的某些组合会造成损坏。希望 USB-C 问题和对它们的记忆也能随着时间的流逝而消失。

[via [Ars Technica](https://arstechnica.com/gaming/2019/08/heres-why-nintendo-switch-consoles-keep-frying)

【主图片来源: [iFixit 任天堂 Switch 拆机](https://www.ifixit.com/Teardown/Nintendo+Switch+Teardown/78263)