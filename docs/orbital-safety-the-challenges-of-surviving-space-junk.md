# 轨道安全:太空垃圾生存的挑战

> 原文：<https://hackaday.com/2021/12/14/orbital-safety-the-challenges-of-surviving-space-junk/>

在地球轨道上闲逛就像走进一场狂野的西部枪战——子弹四处乱飞，即使没有一颗是故意针对你的，也可能有你的名字在上面。这些子弹中有许多是受到主动控制和监控的人造卫星，但我们也发现了死亡的卫星，卫星的残余物，废弃的火箭级，太空行走中丢失的工具，甚至油漆和铁锈的斑点，其中大部分在没有任何引导的情况下以每秒数公里的速度快速移动。

虽然直接清除这些空间碎片是理想的，但现实是，任何必须在轨道上度过时间的航天器和宇航服都需要能够承受空间碎片的撞击。

## 轨道力学

人们很容易产生新的碎片，这一点也不奇怪。可能需要更多一点想象力的是，这些碎片需要多长时间才能到达地球的大气层，并在那里被顺利烧掉。轨道上的一切都在向地球坠落，但它的切向速度阻止了它撞击地球——就像一个弹球在漏斗的孔周围旋转一样。来自行星大气层的阻力是摩擦，最终[使物体减速](https://en.wikipedia.org/wiki/Orbital_decay)，它在行星大气层中的轨道位置决定了这次下降需要多长时间。

[![Orbital decay rate infographic.](img/99d2eb5835954f92e9840439df3e05a7.png)](https://hackaday.com/wp-content/uploads/2021/11/orbital_decay_rate_infographic_ula.jpg)

Orbital decay rate infographic. (Credit: ULA)

正如美国宇航局在 ARES 的轨道碎片项目办公室在他们的 [FAQ](https://www.orbitaldebris.jsc.nasa.gov/faq/) 中引用的那样，轨道上有超过 23，000 个大于 10 厘米的碎片物体，此外还有超过 50 万个 1 厘米到 10 厘米的物体，以及数百万个 1 毫米到 10 毫米的物体。轨道碎片的主要来源是卫星爆炸和碰撞。这包括中国 2007 年的反卫星(ASAT)试验，以及印度 2019 年和俄罗斯 2021 年的 ASAT 试验，这些试验发生在苏联&美国 57 次(总)ASAT 试验之外。

卫星有时会爆炸，比如 2004 年和 2015 年美国 DSMP 卫星爆炸。其他时候，卫星相互碰撞，如铱星-33 与宇宙-2251，被碎片或微陨石击中，等等。因为在低地球轨道，碎片往往以 7 公里/秒以上的速度运行。

根据碎片物体的质量，它与路径上的一颗卫星或其他物体撞击的效果，很可能向相反方向再增加约 7 公里/秒，可能会转移相当于数吨梯恩梯的十亿焦耳动能。事实证明，即使是一点油漆以这样的速度移动，也会造成重大损害，尤其是对太阳能电池板等脆弱的结构。如前所述，这使得这种结构必须能够承受一定程度的冲击损伤。

## 总是小的

[![The Whipple Shield used on NASA's Stardust probe.](img/68bbfa80bf18b655bda8560947969256.png)](https://hackaday.com/wp-content/uploads/2021/11/WhippleShield.jpg)

The Whipple Shield used on NASA’s Stardust probe. (Credit: NASA)

虽然显然携带更多的能量，但较大的碎片的好处是它们相对容易使用地面设备跟踪。如果卫星或空间站过于靠近其中一个大碎片的轨道，它可以使用机载推进器。

这主要留下了较小的碎片，尤其是太小而无法追踪的小薄片和颗粒，但其质量足以造成重大损害。几十年来，航天器的主要保护装置是惠普尔防护罩。很像类似的多重冲击盾，它是一种[间隔盔甲](https://en.wikipedia.org/wiki/Spaced_armour)，这是一种首次在 19 世纪中期的铁战舰上流行的盔甲。

不是简单地使装甲更厚，而是使用多层，在它们之间留有空间或某种填充物。这节省了重量，同时允许进入的射弹无害地消耗其能量。同样的原理可以在国际空间站的窗户上看到，它由多层组成。在 [ISS 的冲天炉](https://en.wikipedia.org/wiki/Cupola_(ISS_module))中，有四层:

*   外部碎片窗格。
*   两块 25 毫米的压力玻璃。
*   内部刮擦板。

外层玻璃应该会消耗大部分撞击能量，其后面的层会挡住碎片云，碎片云的速度应该足够慢，不会造成重大伤害。每个窗口在安装外部覆盖物后都可以在轨道上更换，如果它们遭受如此严重的损坏，更换是有保证的。

[![MMOD damage on ISS solar panel.](img/d38a132774cad1c1a128fc48c738c254.png)](https://hackaday.com/wp-content/uploads/2021/11/international_space_station_mmod_damage_solar_panel.jpg)

Damage observed to ISS solar array 3A, panel 58 (cell side on left, Kapton backside on right). Note by-pass diode is disconnected due to MMOD impact. (Credit: Hyde et al., 2019)

对于国际空间站的其余部分，[弹道板被放置在](https://en.wikipedia.org/wiki/International_Space_Station#Orbital_debris_threats)距离主船体一定距离的地方，其目的是捕获和消散来自微陨石和小轨道碎片的能量。国际空间站上的流星体和轨道碎片损害已经研究了几十年，海德等人在 [2019 年发表的一篇论文描述了最近的发现。](https://www.hou.usra.edu/meetings/orbitaldebris2019/orbital2019paper/pdf/6001.pdf)

一个有趣的发现是国际空间站太阳能电池板的损坏。有一次，一颗微陨石撞击了其中一块面板，造成了一个直径 7 毫米的洞。这破坏了面板中的旁路二极管，并导致电流积聚，最终导致沿三个电池的边缘出现近 40 厘米长的烧穿。

显然，在这种环境下保护太阳能电池板一点也不容易，因为根据定义，在它们前面添加保护板相当于破坏了拥有太阳能电池板的整个目的。国际空间站有超过 250，000 个细胞，预计随着时间的推移，其中一些细胞将不可避免地丢失。2021 年 6 月，国际空间站的宇航员[安装了新的太阳能电池板](https://en.wikipedia.org/wiki/Roll_Out_Solar_Array)来取代最旧的。

虽然像这样更换太阳能电池板是处理空间站累积损坏的一个可行选择，但对卫星来说不太实际，因为卫星应该有足够的过剩电力来应对长期的损失。

## 进攻是最好的防御

由于某些轨道上的碎片会停留几十年或更长时间，我们最终可能会达到主动清除这些碎片的地步。这就是轨道力学和太空中难以置信的空间量使事情变得非常棘手的地方。尽管轨道碎片的风险很高，但由于卫星和碎片都在快速移动，密度非常低。这就是为什么国际空间站上的宇航员看不到碎片一直在飞驰而过。

这种稀疏性使得主动清除碎片成为一项苦差事，并解释了为什么最近的高调任务，如[清除碎片](https://en.wikipedia.org/wiki/RemoveDEBRIS)、[清除空间-1](https://en.wikipedia.org/wiki/ClearSpace-1) 和其他任务专注于在先前已知轨道上运行的大碎片。它们经常要求卫星在距离目标一定距离内移动，并执行精细的操作。如前所述，最大的威胁来自不易追踪的碎片，这似乎在很大程度上挫败了这些清理方法。

在这里，也许最好的方法是不要主动追捕这些物体，而是使用一个庞大的系统被动地捕捉它们，就像蜘蛛如何使用一张网来捕捉毫无防备的猎物。这就是俄罗斯初创公司 StartRocket 和他们的[泡沫碎片捕捉器](https://www.space.com/space-junk-cleanup-foam-satellite-technology.html)的想法。使用泡沫来捕获轨道碎片并不新鲜，2011 年[欧空局的一份报告](https://www.esa.int/gsp/ACT/doc/ARI/ARI%20Study%20Report/ACT-RPT-MAD-ARI-10-6411-Pisa-Active_Removal_of_Space_Debris-Foam.pdf)也深入报道了泡沫的使用。

## 请勿乱扔杂物

即使缓解方案已经到位，轨道碎片清除方法正在研究中，并可能在未来几十年内部署，我们现在能做的最好的事情是防止制造更多的混乱。如今，空间交通管理主要由联合国外层空间事务厅负责，国家政策遵循关于防止轨道碎片和其他考虑的国际协定。

日益关注航天器的可重用性是一个幸运的发展。美国航天飞机计划最宏伟的目标——它将作为一个服务卫星的平台——除了服务哈勃之外从未取得成果。然而，我们可能希望很快看到简单地让整个火箭级到处漂浮的例行丢弃的结束，至少减少一个空间污染源。