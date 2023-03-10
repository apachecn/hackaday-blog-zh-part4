# 一种由钢铁工业废料制成的氧化还原液流电池

> 原文：<https://hackaday.com/2020/05/13/a-redox-flow-battery-made-from-iron-industry-waste/>

南加州大学的研究人员发现了一种方法，可以从钢铁工业的废料中制造出有效且有竞争力的氧化还原液流电池。幸运的是，这篇论文的结果发表在一份公开期刊上，我们可以看看这种电池背后的技术。

随着电力利用、电动汽车的采用和可再生能源的使用不断增加，各地的工程师都在寻找完美的实用规模电池。我们都听说过[特斯拉在南澳大利亚的 100MW](https://hackaday.com/2019/12/16/the-hornsdale-power-reserve-and-what-it-means-for-grid-battery-storage/) 锂电池组。该系统取得了巨大的成功，并已经收回了成本。然而，所有的工程师都很快指出，在我们取得突破之前，从长远来看，锂电池并不是公用事业系统的正确选择。一定有更好的解决办法。

## 好的电池应该是什么样的？

[![](img/914ed7a8037f32c2aa242c395dcf2860.png)](https://hackaday.com/wp-content/uploads/2020/05/Vanadium_Redox_flow_battery.jpg)

A Vanadium Redox flow battery located at the University of New South Wales. Credit: [Radiotrefoil](https://en.wikipedia.org/wiki/Vanadium_redox_battery#/media/File:Vanadium_Redox_flow_battery.jpg)

网格规模存储是一个重要且难以解决的问题。如果我们没有电池，我们就无法远离化石燃料发电。如果没有电网存储，每一次电力浪涌，比如英国打开茶壶喝茶，都会使电网瘫痪。

目前，发电厂整天上下运转，以满足需求。即使我们在地平线上没有可再生能源，更好的电池将允许我们更有效地运行更小的发电厂来满足需求。你可以全天以最高效率运行一个工厂，电池可以平衡负载。这是你的汽车的燃油经济性之间的差异，如果你在城市减速和加速，或在高速公路上保持巡航速度。

理想的电池有几个要求。它必须以合理的速度充电。它还需要能够立即传递电荷。最重要的是，电池必须便宜，续航时间长。这简直是不可能的又快又好又便宜的困境。工程师们已经尝试了从熔盐到堆积岩石的各种方法。例如，水电站大坝只不过是由水和重力组成的电池。特斯拉的大型电池由锂离子电池制成。

选择这种系统的主要经济决策驱动因素是能量存储(LCOS)的平准化成本。这是系统的资本成本和运行成本与系统生命周期内储存和输送的总能量之和。该论文提到，美国能源部规定了 2.5 美分/千瓦时的 LCOS 目标。以 200 美元/千瓦时的安装成本计算，电池在其寿命期间必须提供 8000 千瓦时的能量。正如作者指出的，如果你考虑一天一次充放电循环，这意味着电池应该可以使用 22 年。我们知道锂电池无法应对这一挑战。

## 氧化还原液流电池

[![A diagram from the paper showing the operation of a typical flow battery.](img/863d465c716e926bd811ca2c25903b29.png)](https://hackaday.com/wp-content/uploads/2020/05/2020-05-05_16h46_48.png)

A diagram from the paper showing the operation of a typical flow battery.

还有另一种电池，我们之前讨论过，叫做氧化还原液流电池。这种电池有无限使用寿命的潜力，运行成本低，甚至可能是生态友好的。

![The chemicals can be two separate chemicals, the same one, or any arbitrary blend. This affects how efficient the battery is and how hard it is to recycle/refresh the chemicals used during operation.](img/90ad06eb30f65e5a7b802506f156096f.png)

The chemicals can be two separate chemicals, the same one, or any arbitrary blend. This affects how efficient the battery is and how hard it is to recycle/refresh the chemicals used during operation.

在这种电池中，两种化学物质被一层膜隔开，相互流过。根据你在化学物质中放置电极的方式，质子穿过膜从一个容器到另一个容器，在两者之间建立电势差。所用的物质可以是相同的化学物质，也可以是不同的化学物质，甚至是两者的混合物。

氧化还原电池的当前技术状态是基于钒。最大的装机容量在日本，为 60 兆瓦时。然而，中国真正令人印象深刻的电力基础设施超级公司目前正在建设 800 兆瓦时的装机容量。然而，钒并不便宜，而且这种材料还有点毒性。

## 铁电池

还有一种元素在这些电池中发挥着奇妙的作用，那就是铁。它只是在等待一个突破，让它在规模上运行，这就是研究人员有了突破。他们发现，他们可以使用铁工业的副产品硫酸铁和蒽醌二磺酸作为大桶两侧的化学物质，并获得非常有效的氧化还原电池。

除了电池电压较低之外，它还具有钒电池无法比拟的优势。这意味着电池装置必须更大、更复杂，但最终会更便宜，因为初级电解质是相对安全的工业分支，电池具有对称系统的简单性:膜两侧的化学混合物是相同的，使溶液更新容易。作者估计，这种电池的成本为 54 美元/千瓦时，而目前最先进的钒电池徘徊在 160 美元/千瓦时至 180 美元/千瓦时之间。这是一个不错的降价。

这些电池是令人着迷的技术。它们也令人惊讶地可以被黑客攻击。当然，一些获得最大效率的步骤，比如用碳纳米管掺杂薄膜，可能需要[【本·克拉斯诺】级别的黑客](https://hackaday.com/2018/04/03/ben-krasnow-tests-novel-plasma/)。但是基本的电池[可以用废料](https://hackaday.com/2016/11/05/see-if-you-can-reverse-engineer-this-scrap-metal-battery/)制成，这很好地表明了这项技术的可行性。我们很好奇储能革命将如何改变未来的世界。你怎么想呢?