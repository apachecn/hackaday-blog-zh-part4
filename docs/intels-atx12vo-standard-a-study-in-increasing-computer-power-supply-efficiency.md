# 英特尔的 ATX12VO 标准:提高计算机电源效率的研究

> 原文：<https://hackaday.com/2021/06/07/intels-atx12vo-standard-a-study-in-increasing-computer-power-supply-efficiency/>

古老的 ATX 标准是由英特尔在 1995 年开发的，试图将当时围绕 IBM AT PC 遗产形成的 PC 生态系统标准化。前面的 AT 外形与其说是一个标准，不如说是对 IBM AT 的近似主板及其所有缺陷的复制。

随着 [ATX](https://en.wikipedia.org/wiki/ATX) 标准的出现，ATX 电源(PSU)也应运而生，该标准定义了标准电压轨和每个附加功能的功能，如软电源开启(PS_ON)。与 20 世纪 90 年代及以后的所有电器和小工具一样，ATX PSU 成为能效法规的主题，这也导致了 2004 年的 80+认证计划。

从 2019 年开始，英特尔一直在为新系统推广 ATX12VO(仅 12 V)标准，但这个新标准是关于什么的，将一切都切换到 12 V 真的值得节省任何功耗吗？

## ATX12VO 是什么

顾名思义，ATX12VO 标准本质上是去除 ATX PSU 标准中目前存在的其他电压轨。这个想法是，通过提供一个单一的基础电压，任何其他电压可以根据需要使用降压转换器产生。自奔腾 4 时代以来，这已经成为处理器和主板上许多电路的标准做法。

随着 ATX PSU 标准从旧的 1.x 修订版转变为当前的 2.x 修订版，取消了-5V 供电轨，并使-12V 供电轨成为可选供电轨。主板的 ATX 电源连接器从 20 针增加到 24 针，以允许增加更多的 12 V 容量。随着奔腾 4 对电源的需求而来的是新的 4 针主板连接器，它通常被称为“P4 连接器”，但在 v2.53 标准中正式称为“+12 V 电源 4 针连接器”。这又增加了两条 12 V 线路。

[![](img/8956997921cf0f7bd468683a6e8fdb44.png)](https://hackaday.com/wp-content/uploads/2021/05/atx12vo_mainboard_power_io.jpg)

Power input and output on the ASRock Z490 Phantom Gaming 4SR, an ATX12VO mainboard. (Credit: [Anandtech](https://www.anandtech.com/show/15763/first-atx12vo-consumer-motherboard-the-asrock-z490-phantom-gaming-4sr))

在 ATX12VO 标准中，删除了-12 V、5 V、5 VSB(待机)和 3.3 V 供电轨。24 针连接器被一个 10 针连接器取代，除了新的 12 VSB 备用电压轨之外，该连接器还承载三条 12 V 线(比 ATX v2.x 多一条)。4 针 12 V 连接器仍然存在，仍然需要一个人通过系统外壳上不可能的小间隙挤压一两个连接器，才能将它们连接到主板顶部，靠近 CPU 的电压调节器模块(VRM)。

虽然 PSU 本身会有些精简，但主板会获得 5 V 和 3.3 V 轨道的 VRM 部分，以及 SATA，Molex 和类似产品的功率输出。本质上，主板将接管 PSU 的一些功能。

## 为什么 ATX12VO 存在

[![](img/540b56736d2ac7016c2ce99838a60780.png)](https://hackaday.com/wp-content/uploads/2021/05/dell_computers.jpg)

A range of Dell computers and server which will be subject to California’s strict efficiency regulations.

GamersNexus 的人在去年发表的一篇文章和一段视频中讲述了他们的研究和业界对 ATX12VO 主题的想法。长话短说，OEM 系统制造商和系统集成商受到非常严格的能效法规的约束，尤其是在加利福尼亚州。从 2021 年 7 月开始，新的 Tier 2 法规将生效，对 OEM 和 SI 计算机设备增加了更严格的要求:详见 [1605.3(v)(5)](https://energycodeace.com/site/custom/public/reference-ace-t20/Documents/section16053statestandardsfornonfederallyregulatedappliances.htm) (具体见表 V-7)。

为了满足这些越来越严格的效率要求，原始设备制造商一直在开发他们自己专有的 12 V 专用解决方案，如 GamersNexus 的[最近关于戴尔 G5 5000 预构建台式机系统的视频评论](https://www.youtube.com/watch?v=4DMg6hUudHE)中所述。因此，英特尔的 ATX12VO 标准似乎更倾向于统一这些专有标准，而不是取代 DIY 系统中的 ATX v2 . x PSU。对于后一类人，他们用标准的 ATX、迷你 ITX 和类似的部件建造自己的系统，这些严格的效率规定并不适用。

因此，首要问题是 ATX12VO 对 DIY 系统构建者是否有意义。虽然(理论上)提高能效(尤其是在低负载时)的能力似乎很有益，但使用 ATX v2 . x PSU 也并非不可能。正如一位匿名的 PSU 制造商在 GamersNexus 文章中所述，si 很可能最终只是使用高效的 ATX v2 . x PSU 来满足加利福尼亚州的 Tier 2 法规。

## 进化与革命

[![](img/1f356f4157d43c30c98dc5079bd7af98.png)](https://hackaday.com/wp-content/uploads/2021/05/CONNECT-vertical.png)

Seasonic’s CONNECT DC-DC module connected to a 12V PSU. (Credit: Seasonic)

自最初的 ATX·PSU 标准以来，改进一直是渐进的，从未中断过。虽然有些人在试图为依赖-5 V 和-12 V 供电轨的旧主板供电时被遗漏的负电压供电轨所困扰，但总体而言，这些变化很小，足以将它们纳入计算机系统的自然升级周期。ATX12VO 则不然，因为它绝对需要 ATX12VO PSU 和主板来实现更高的效率目标。

虽然存在使用 ATX v2.x 到 [ATX12VO 适配器](https://www.corsair.com/us/en/Categories/Products/Accessories-%7C-Parts/PC-Components/Power-Supplies/ATX12VO-Adapter-Cable/p/CP-8920272)的可能性，即被动地将 12 V 轨适配到新的 10 引脚连接器，并将 5 VSB 线提升到 12 VSB 电平，但这实际上降低了效率，而不是提高了效率。从本质上来说，ATX12VO 有意义的唯一方式是行业立即转变，每个人都升级到它，而不重用不兼容 ATX12VO 的主板和 PSU。

这里的另一个关键点是，并不要求 OEM 和 si 采用 ATX12VO。就像英特尔命运多舛的 BTX 替代 ATX 标准一样，ATX12VO 是一个建议标准，制造商和原始设备制造商可以随意采用或忽略。

这里重要的可能是 ATX12VO 引入的明显的负面因素:

*   给主板增加了另一个热点并占用了宝贵的主板空间。
*   把主板制造商变成 PSU 制造商。
*   增加了主板的成本和复杂性。
*   从主板布线外围电源(包括机箱风扇)。
*   电源问题的故障排除变得复杂。

[![](img/f536ee45a45c22c9c68f2cf281eedab4.png)](https://hackaday.com/wp-content/uploads/2021/05/seasonic_connect_internals.jpg)

Internals of Seasonic’s CONNECT modular power supply. (Credit: [Tom’s Hardware](https://www.tomshardware.com/reviews/seasonic-connect-750w-power-supply))

除此之外，还有潜在的替代产品，如 [Seasonic 的 CONNECT](https://seasonic.com/connect) 模块。这实际上与 ATX12VO 标准相同，从 PSU 中移除 5 V 和 3.3 V 轨，并将它们移动到主板之外的外部模块。在许多电脑机箱中，它可以安装在主板后面的区域，使电缆管理非常干净。它还可以提高效率。

由于 PSU 往往至少能经受几次系统升级，因此从环境角度来看，在主板上生成次轨是不可取的。也许 ATX12VO 最不可取的方面是它降低了 ATX 式计算机的模块化本质，使它们更像笔记本式系统。相反，更合理的解决方案可能是类似 CONNECT 的解决方案，它提供 ATX 24 引脚和 ATX12VO 风格的 10 引脚连接选项。

## 胸怀大志

在更大的电源效率方案中，从计算机系统内部等细节后退几步，看看为这些系统供电的交流电源(AC)等，可能是有益的。与任何现代计算机中使用的开关模式电源(SMPS)一样，开关模式电源的一个众所周知的特性是，它们在较高的交流输入电压下效率更高。

[![](img/986f0da531e3d549f23c7fc846d77db2.png)](https://hackaday.com/wp-content/uploads/2021/05/power_supply_efficiency_voltage_range_hp.jpg)

Power supply efficiency at different input voltages. (Credit: HP)

这一点在查看 [80 加](https://en.wikipedia.org/wiki/80_Plus#Efficiency_level_certifications)认证的评级级别时可以清楚地看到。在 120 VAC 和 230 VAC 线电压之间，后者明显更有效。此外，与 230 伏交流电压相比，在 120 伏电压下，同样的功率消耗，在室内布线上携带两倍的安培数也会增加电阻损耗。根据[这份 APC 白皮书](http://www.apc.com/salestools/SADE-5TNQZ7/SADE-5TNQZ7_R3_EN.pdf)，这就是为什么北美的数据中心通常使用 208 VAC 运行的原因。

对于加密矿工和类似的人来说，用 240 VAC(北美热-中性-热)给他们的机房布线也是一个热门话题，因为这直接增加了他们的利润。

## 未来展望

ATX12VO 是会成为下一个大事件，还是会像 BTX 和其他许多提议的标准一样失败，这很难说。ATX12VO 标准反对它的一点是，它肯定需要并行发生许多重大变化，并且在短时间内通过强制升级产生大量电子垃圾。如果我们考虑到许多 ATX 和 SFX 风格的 PSU 提供 7-10 年保修，而主板的寿命要短得多，这就构成了一个重大障碍。

根据业内的声音，似乎很有可能大部分将保持“一切照旧”。有许多高效的 ATX v2 . x PSU，包括 80 Plus 白金和钛级 PSU，Seasonic 的 CONNECT 和类似的解决方案对那些喜欢整洁的电缆管理的人有很大的吸引力。对于那些购买预建系统的人来说，ATX12VO 的使用也是不相关的，只要硬件符合所有(效率)法规。ATX v2.x 标准和 80 Plus 认证也在改变，以设定严格的 2-10%负载效率目标，这是 ATX12VO 的主要目标。

您选择 ATX12VO 的原因是什么？如果两者都提供相同的效率水平，您会选择 atx 12vo 而不是 Seasonic CONNECT 这样的解决方案吗？

(**标题图片**:连接 SATA 电源的 Asrock Z490 Phantom Gaming 4SR，信用:[c t](https://www.ct.nl/achtergrond/wat-is-atx12vo-nieuwe-standaard-voeding/)