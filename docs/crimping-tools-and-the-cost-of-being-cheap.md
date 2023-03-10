# 压接工具和低廉的成本

> 原文：<https://hackaday.com/2022/02/07/crimping-tools-and-the-cost-of-being-cheap/>

压接连接器提供了一种简单方便的方式来连接电子设备，同时还允许在无需触及烙铁和脱焊芯的情况下移除和交换电子设备。在浏览一个人最喜欢的廉价购物网站时，你可能会得到这样的印象:要加入 crimp-awesome 的世界，你只需订购一个 20 美元的压接工具和一些配套的“JST”和“DuPont”(一种迷你光伏克隆)连接器。毕竟，它只是挤在一些剥开的电线周围的一点金属。这能有多复杂？

残酷的事实是，尽管官方 JST 和 Mini-PV 压接工具上的价格标签可能看起来高达数百美元，但它们提供了精确、可重复的压接和可靠的长期稳定性。正品 JST、Mini-PV、Molex 连接器也是如此。“省一美元”的价格标签最终可能会比最初省下的钱高得多。

## 警示故事

[![](img/184ca8efb63638e43e4a19ff7534ea4d.png)](https://hackaday.com/wp-content/uploads/2022/01/media-1200354-bad-crimp-bad-news-fig3.jpg)

Example of the improper crimp (left) that caused fires in AC units. Contrast with right crimp and lack of spacing.

回到 2007 年 12 月，安装在汽车旅馆和公寓里的空调设备开始着火，看起来是自己着火了。所有这些空调设备都是由一家德州公司制造的:古德曼公司。在多次报告设备着火后，人们推断这一定是来自新供应商 Tower 的有故障的电源线。

在召回了使用塔式供电电缆的设备后，接下来的法律诉讼和调查试图确定火灾的原因。使用尚未着火的设备，原因被追溯到电源线绞线上卷曲的标志连接器。由于压接过程中施加的压力不足，在标记连接器内留下了空间，增加了接触电阻。

吸取大量的电流，这将导致快速的热发展，最终火灾。塔架工厂使用的不是指定的 AMP 压接机，而是配置不当的仿制机，导致压接不当。在这种情况下，Tower 为了节省一些钱而做出的决定最终让他们损失了大量收入，并危及了生命和财产。

良好压接的基本要素是[塑性变形](https://en.wikipedia.org/wiki/Plasticity_(physics))的要素:相关材料的自然塑性，以及这种塑性是否被充分利用以获得牢固的接触，但没有(破坏性地)超过或——在这种情况下——几乎没有使用。

## 货物出门概不退换

前面的例子清楚地表明，你必须非常谨慎地对待你要买的东西:不仅是工具，还有组件。一个很好的例子是山寨连接器，人们可以亲切地称之为“杜邦综合症”，这是一个更好的连接器的廉价克隆，比原来的连接器更有名。

[![De-constructed Mini-PV contact and Be-Cu leaf spring (left) and “DuPont” clone (right). (Credit: Matt Millman)](img/e219653142fe6d6756f435409ce38308.png)](https://hackaday.com/wp-content/uploads/2022/01/minipvdecon-800x417-1.jpg)

De-constructed Mini-PV contact and Be-Cu leaf spring (left) and “DuPont” clone (right). (Credit: Matt Millman)

据马特·米尔曼称，伯格电子公司在 20 世纪 50 年代推出了他们的迷你光伏连接器。这是一个可能会被误认为“杜邦”连接器的连接器，但事实上是一个更好的[连接器](https://www.connectortips.com/breakthrough-contact-design-spawned-500m-connector-company/) r，具有[双金属设计](http://www.mattmillman.com/info/crimpconnectors/dupont-and-dupont-connectors/)，包括一个 BeCu 板簧，今天仍由 Amphenol 生产，包括为美国军方和美国政府的其他部门生产。

伯格电子公司于 1972 年被杜邦公司收购，成为后者的一个部门。这可能解释了为什么在 20 世纪 90 年代更便宜、受微型光伏启发的克隆连接器开始出现时(包括 Harwin 制造的带有 [M20](https://www.harwin.com/connectors-hardware/pcb-connectors/2-54mm-pitch-pcb-connectors/) 的连接器)，它被称为“杜邦连接器”，尽管它在机械上不同于微型光伏连接器。

从那时起，克隆制造商不仅开始生产他们自己版本的“杜邦”连接器，还生产 [JST 的产品](http://www.mattmillman.com/info/crimpconnectors/common-jst-connector-types/)，包括他们的 XH、PH 和其他系列。公差，使用的材料和其他规格，如涂层，因此任何人都可以猜测，特别是当从上述廉价购物网站上的匿名卖家那里购买时。

在连接器中使用不同金属的问题是[电偶腐蚀](https://en.wikipedia.org/wiki/Galvanic_corrosion)。虽然这在短期内很少成为问题，但根据环境条件，在 PCB 和线束上使用不同电镀的连接器可能会在几个月到几年后导致故障累积。如果不知道项目中使用的连接器和布线的确切规格，这将成为一个重大风险，当长期可靠性非常重要时，绝对应该避免。

## 挤压金属而不是预算

就像在便宜的仿制连接器上省下几块钱一样，了解便宜的压接工具的问题是很重要的，这些问题主要是压接效果不理想，偶尔会出现未受过专业训练的人无法发现的有缺陷的压接。作为一个恰当的例子，让我们来看看一种比“JST”和“DuPont”更好的压接工具——您最近也获得了这种工具 Matt Millman 对其进行了审查和比较:“Preciva PR-3254”:

[![Preciva PR-3254 crimp tool. (Credit: Matt Millman)](img/0fc1315b6f6627062abebde335081d62.png)](https://hackaday.com/wp-content/uploads/2022/01/preciva_crimping_tool_pr-3254.jpg)

Preciva PR-3254 crimp tool. (Credit: Matt Millman)

作为真正的 Berg/DuPont Mini-PV 压接工具的所有者，Matt 能够对这两种工具及其压接结果进行并排比较。注意到最重要的细节是 PR-3254 具有正确的模具形状，因为“DuPont”部分的顶部必须是“O”形，而不是“B”形，这是 JST 压接工具的正确形状。

[![Comparison of the DuPont Mini-PV crimp tool, and the die of a typical budget tool. (Credit: Matt Millman)](img/77188fcde6ef8f1583db04a87d76fb91.png)](https://hackaday.com/wp-content/uploads/2022/01/upperjaw-800x421-1.jpg)

Comparison of the DuPont Mini-PV crimp tool, and the (improper) die of a typical budget tool. (Credit: Matt Millman)

不幸的是，当你靠近看时，它并不完全是正确的形状。问题出现在钳口闭合时，产生的空间更像椭圆形，而不是杜邦压接工具的圆形:

[![PR-3254 “DuPont” die compared to DuPont HT-208 (AWG 24) die. (Credit: Matt Millman)](img/a719d9ee27e58111ffd5cab4fc505661.png)](https://hackaday.com/wp-content/uploads/2022/01/pr-3254_ht-208_die_comparison.jpg)

PR-3254 “DuPont” die compared to DuPont HT-208 (AWG 24) die. (Credit: Matt Millman)

虽然产生的压接是可接受的，但当使用 AWG 24 (0.205 mm ² )导线时，它确实会压碎绝缘，而使用 AWG 28 (0.0810 mm ² )导线时，绝缘压接良好，但导线本身的力不足。这可能导致接触电阻增加和其他问题。

[![Harwin Z20-320\. Crimps “DuPont” clone types effortlessly and perfectly. It’s made by Pressmaster in Sweden. (Credit: Matt Millman)](img/547f76c4ebbe6a4c544908f47e927faa.png)](https://hackaday.com/wp-content/uploads/2022/01/z20-320-800x606-1.jpg)

Harwin Z20-320\. Crimps “DuPont” clone types effortlessly and perfectly. It’s made by Pressmaster in Sweden. (Credit: Matt Millman)

在审查另一款声称针对“杜邦”连接器的经济型压接工具( [IWISS SN-025](http://www.mattmillman.com/iwiss-sn-025-another-head-scratching-dupont-crimp-tool-lands/) )时，Matt 发现它比 PR-3254 要好一些，但通常不应用于任何关键应用。除非有人有兴趣成为不负责任的制造商名单中的另一个条目，就像 Tower 一样，这可能是一个好主意，花 460 美元购买像官方 Harwin M20 Z20-320 压接工具这样的东西。

这些工具提供的功能包括诸如电线挡块这样的细节，以便您不能将待压接的连接器插入太远，以及模具内的各种导轨，这些导轨有助于在压接之前和压接期间稳定连接器。这具有巨大的好处，即每个压接可能尽可能接近完美，而对于手动(非棘轮)工具和廉价压接工具，需要一定水平的技能来获得甚至可接受的结果。

## 底部挤压

或许最重要的是，在深入了解压接连接器和相关工具的本质之前，有必要了解基本知识。这不仅是为了避免被那些不能胜任其购买任务的组件和工具所拖累，也是为了防止更糟的情况发生。即使这只是一个爱好项目，对自己的卷发的中长期可靠性有一些信心也是非常可取的。

尽管压接连接器应该而且能够快速且几乎毫不费力地完成，但劣质的元件和/或工具肯定会浪费相关人员的时间。当谈到选择任何一个时，这都归结为一个有意识的选择:得到哈文 M20 迷你光伏克隆，还是赌一把全球速卖通上随机卖家当天有什么存货？IWISS 或 Preciva 工具是否是正确的选择，因为它“只是为了一些修补”，或者错误的压接可能会导致潜在的非常糟糕的后果？

很自然，简单的答案就是花钱购买官方的 Harwin、JST 和 Molex 零件和工具，但即使有人在 EBay 上找到了使用的压接工具，这仍然是一笔很大的投资，因为这可能只是一种“爱好”，失败并不严重。只要意识到所用零件和工具的局限性，除了使用会损坏连接器和/或电线的廉价压接工具之外，可能没有什么真正糟糕的选择。

【标题图片:一大堆压接工具。(鸣谢:马特·米尔曼)]