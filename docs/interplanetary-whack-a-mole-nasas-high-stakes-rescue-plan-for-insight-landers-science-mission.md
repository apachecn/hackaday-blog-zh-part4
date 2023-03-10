# 星际打地鼠:美国宇航局 InSight 着陆器科学任务的高风险救援计划

> 原文：<https://hackaday.com/2020/03/12/interplanetary-whack-a-mole-nasas-high-stakes-rescue-plan-for-insight-landers-science-mission/>

人们有理由对现代外科技术感到惊叹，这种技术让外科医生能够利用机器人的力量，通过可以缝合几针的伤口来修复人体的最小结构。这种技术甚至可以远程应用，通过远程手术连接外科医生和机器人。这可能有风险，但通常是病人的唯一选择。

美国宇航局也到了类似的拐点，只不过他们的病人是火星 *InSight* 着陆器，手术套件目前距离大约 5800 万公里。着陆器的自挖掘“鼹鼠”探测器需要一点帮助才能启动，因此他们计划进行一次高风险的救援尝试，这将使最有经验的远程手术变得苍白无力:他们希望使用着陆器的机械臂向下按压鼹鼠，以帮助它回到轨道上。

## 关于摩擦的一切

[![](img/3e4bdf653c601368ad57c75c6b3cd007.png)](https://hackaday.com/wp-content/uploads/2019/10/mole.gif)

Mole at work. Rendering of the HP³ penetrator mechanism. Source: [German Aerospace Center, DLR](https://www.youtube.com/watch?v=KAxiHK6dYvE)

我们已经讨论 InSight 有一段时间了，从[开始讨论](https://hackaday.com/2019/08/07/holey-moley-fixing-the-mars-insight-mole/)作为热流和物理特性包(HP)实验的一部分，mole 应该如何工作。简单回顾一下，鼹鼠基本上是一个电动冲击驱动器，带有一个旋转凸轮，它加载一个弹簧，将机械能释放到一个重锤中。撞击应该会将鼹鼠一次推进火星风化层几毫米，缓慢地钻入风化层五米，同时拖着一条装满传感器的尾巴，以测量地下热流。

不幸的是，惠普一直无法深入土壤。这次失败被归因于各种原因，从撞击地表下的岩石到之前未知的榴石壳层，这是一种由土壤颗粒组成的坚硬层，这些土壤颗粒通过曾经在火星上自由流动的水中的化学沉淀物粘合在一起。除了这些可能性之外，事实证明火星土壤的粘结性远不如最初想象的那样强，给了鼹鼠很小的工作摩擦力，难怪它会被卡住。

回到 2019 年 10 月，看起来鼹鼠又开始行动了。JPL 的工程师们决定在鼹鼠试图挖掘时，用着陆器的机械臂压住它的船体。他们的想法是，增加摩擦力会给它所需的推动力来穿透榴莲皮并再次前进。

## 打地鼠

最初的报道是鼹鼠在这次牵制行动后取得了进展，但这被证明是乐观的。鼹鼠确实取得了进展，但它有两次从洞里蹦了出来。这些失败为当前最危险的想法扫清了道路:使用机械臂的铲子直接推动鼹鼠的后帽。

[![](img/440f01ba44cd0ace96536c970b965aa6.png)](https://hackaday.com/wp-content/uploads/2020/03/480px-PIA23213-Mars-InSightLander-MoleBacksOutOfHole-20191026.gif)

Pinning was working, but the mole popped back out. Source: [NASA/JPL](https://photojournal.jpl.nasa.gov/archive/PIA23213.gif)

从表面上看，这似乎是最有意义的方法。毕竟，如果鼹鼠向下移动有困难，向下施力应该有助于它穿透榴莲皮。但这并不像推一把鼹鼠那么简单。

首先考虑问题的物理方面。这只鼹鼠的直径约为 3.5 厘米，这是一个非常小的目标，可以用机械臂的铲子击中。就操作而言，后盖也不是最友好的表面。它被鼹鼠的尾巴一分为二，看起来像一个柔性的 Kapton PCB。尾巴一侧的后帽上也有一个突起，这似乎限制了勺子压住鼹鼠的能力。

尾巴本身也是个问题。需要特别小心，确保勺子不会接触到柔性 PCB，如果被夹住，柔性 PCB 可能会受损。尾巴不仅为鼹鼠提供动力，还提供数据连接；失去其中的任何一个，你都有可能失去这个任务。定位勺子必须非常小心翼翼地进行，并且已经在地球上的实体模型上进行了实践，并使用了火星上的实际硬件。

[![](img/dcf58552c95ae77633a77beeffcc7aed.png)](https://hackaday.com/wp-content/uploads/2020/03/24780_PIA23619-16.jpg)

Testing the push maneuver on Earth-side simulator. Source: [NASA](https://mars.nasa.gov/news/8612/mars-insight-lander-to-push-on-top-of-the-mole/?site=insight)

延迟肯定也会成为一个大问题。目前从地球到火星的无线电信号往返时间超过 6 分钟，这意味着实时控制操作将是不可能的。移动必须事先仔细计划，并以非常小的增量进行，以尽量减少损坏的机会。

从一开始，通过工程上的独创性从失败的深渊中夺取胜利就是太空探索的故事，所以工程师们很有可能在不损坏鼹鼠的情况下推进它。星际打地鼠游戏是否会有结果谁也说不准，但即使惠普永远没有机会深入火星，也不会因为没有尝试过。