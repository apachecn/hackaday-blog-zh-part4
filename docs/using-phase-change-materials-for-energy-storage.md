# 使用相变材料进行能量存储

> 原文：<https://hackaday.com/2021/03/03/using-phase-change-materials-for-energy-storage/>

可再生能源越来越受欢迎。然而，如果在不需要的时候有多余的能量，这种能量就会被浪费掉。一个特别相关的例子是太阳能；太阳能电池板在白天提供大部分输出，而一个家庭最大的能源消耗通常是在晚上。

解决这个问题的一个方法是储存多余的能量，以便以后使用。最常见的方法是使用大电池，然而，这并不是镇上唯一的游戏。相变材料被证明是储存多余能量并在以后回收的有用工具——不是以电的形式储存能量，而是以热的形式储存能量。让我们看看这项技术是如何工作的，以及它的一些最有用的应用。

## 这都是因为热

[![](img/eea3eb986884b8108a2f780e80122f9a.png)](https://hackaday.com/wp-content/uploads/2021/02/phase-watergraph.gif)

The heating curve of water. Note the flat lines on the curve where the latent heat must be overcome to change phase.

与电池或电容器不同，相变材料不是以电的形式储存能量，而是以热的形式储存能量。这是通过利用相变的独特物理性质实现的——在材料在固相和液相或液相和气相之间转变的情况下。当热能作用于一种物质时，例如水，温度就会升高。然而，当液态水达到接近沸点的温度时，奇怪的事情发生了。

随着更多的能量进入，温度开始趋于平稳。这是因为必须输入足够的能量来克服所谓的*汽化潜热*——将液体变成气体所需的能量。最终，一旦足够的热量进入，水变成蒸汽，温度再次自由上升。这种潜热可以在相对较小的温度变化下在材料中储存大量的能量。这种潜热也存在于固态到液态的相变中，我们称之为熔化潜热。通过利用潜热，大量的能量可以存储在实际温度的相对较小的变化中，并通过操纵材料的相变来获取。

也许市场上最常见的相变蓄热形式是醋酸钠手摇加热器。这些洗手器在一个塑料袋里装有一种醋酸钠凝胶。当通过调整凝胶中的金属盘给凝胶一个成核点时，它会迅速从过饱和液体变成固体。像这样的突然冷冻释放了这种材料在液态时的潜在热量，温暖了使用者的双手。这种材料以后可以通过加热手持设备再次熔化醋酸钠，然后让它慢慢冷却到室温。潜在的热量将被截留在液体中，直到它再次被扰乱，导致它再次冻结。

[通过相变效应](https://www.researchgate.net/publication/222680528_A_review_on_phase_change_energy_storage_Materials_and_applications)对各种各样的材料进行了储热研究。石蜡可能是最常被研究的一种，因为它的相变发生在一个有用的温度范围内。然而，它的低导热性限制了能量交换的速度，从而影响了性能。水合盐是另一种有重要意义的材料，尽管面临着自身的问题。通常，这些材料会经历过冷。随着热量从液体材料中被提取出来，液体材料的温度下降到冰点以下，而液体材料实际上并没有变成固体。在没有经历相变的情况下，潜热仍然滞留在液体中，不能被提取。此外，像许多电池化学物质一样，重复循环会引起问题。相变材料必须在多次循环后保持其特性，不会随着时间的推移而有化学物质从溶液中析出或腐蚀损害材料或其外壳。对相变储能的许多研究都集中在提炼解决方案以及使用添加剂和其他技术来应对这些基本挑战。通常，这些材料的细节仍然是商业秘密，因为公司试图通过销售收回研究成本。

![](img/244ccaaa1c263533f15b972ee16fa176.png)

Sunamp’s early phase change cells for home heating – note the input and output fluid ports that feed into the internal heat exchanger.

相变效应可以以多种方式用于功能性存储和节能。热量可以施加到相变材料上，使其熔化，从而将能量以潜热的形式储存在其中。过剩的电能，例如来自可再生资源的电能，可以很容易地储存在这种相变材料中，因为它可以非常有效地将电能转化为热能。然而，反过来就不那么容易了。

相反，这种相变装置通常被用来更直接地输出热量——或者通过[被用作热水加热器](https://www.bbc.com/news/uk-scotland-40188414)或者通过[向制冷过程](https://arena.gov.au/assets/2017/02/maximising-solar-pv-phase-change-thermal-energy-storage.pdf)提供热能。这通常通过简单地将工作流体如水或制冷剂通过与相变材料接触的热交换器来实现。前者对家庭有很大的适用性，减少了住宅供暖和热水的费用。后者与大型商业和工业设施更相关。特别是在酿酒和冷藏等行业，制冷可能是运营中必不可少的主要底线支出。随着时间的推移，即使很小比例的效率提升或能源使用的减少也会带来巨大的回报。

![](img/3cdb41f93be60445964d0cd014f4bb41.png)

Different phase change materials freeze at different temperatures, making them suitable for different applications. Lower-temperature materials are useful for refrigeration applications such as in this project by the University of South Australia.

相变材料的另一个有趣用途是作为建筑物的被动热管理解决方案。这个想法是使用熔点在舒适室温附近的相变材料，比如 20-25 摄氏度。这种材料被封装在塑料垫子中，可以和绝缘材料一起安装在建筑物的墙壁和天花板上。这种材料可以作为一种热缓冲。相变材料可以吸收房间里积累的热能，保持较低的温度。当建筑冷却时，这种材料可以释放热量，起到稳定温度的作用。它可以是增加建筑物热质量的一种轻质方法，并且可以减少对 HVAC 系统的主动冷却或加热的依赖。

![](img/93b5a6455eb79144e1bed4de60630600.png)

BioPCM brand phase-change material installed in a ceiling. This is used as a lightweight way to add thermal mass to a building, helping maintain stable comfortable temperatures without the need for continuous heating and cooling.

展望未来，相变储能在住宅空间中的应用可能仍然有限。虽然它有好处，但它有限的仅用于加热的应用使它不如可以运行整个家庭的电池存储有吸引力。然而，对于工业过程，如制冷和过程加热，相变技术作为一种廉价而有效的储能技术有很大的应用空间。随着该领域的研究不断深入，随着未来几年节能的相关性增加，我们很可能会看到这项技术在未来被更多地采用。