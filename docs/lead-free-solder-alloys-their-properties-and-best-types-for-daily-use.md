# 无铅焊料合金:它们的性能和日常使用的最佳类型

> 原文：<https://hackaday.com/2020/01/28/lead-free-solder-alloys-their-properties-and-best-types-for-daily-use/>

自从人类开始焊接以来，无铅焊料合金就一直存在，其来源[可以追溯到大约 5000 年前](https://web.archive.org/web/20120425153916/http://www.weldinghistory.org/whistoryfolder/brazing/bh_pre1900s.html)。这些合金大多是铜-银或银-金的混合物，并与所谓的硬焊接一起使用。这是一种至今仍在使用的将贵金属和半贵金属连接在一起的技术。最近的发展是使用“软焊接”将电子元件焊接在一起，这需要更低的温度。

早期的软焊接使用纯锡(Sn ),然而[逐渐寻求合金](https://hackaday.com/2019/05/30/the-fascinating-world-of-solder-alloys-and-metallurgy/),以解决锡基合金中的热循环、抗冲击、电子迁移和晶须发展等问题。虽然铅(Pb)能够在大多数焊接应用中发挥这一作用，但产品中铅的逐步淘汰以及对间距越来越小的元件的新要求要求开发新的焊料合金来发挥这一作用。

在本文中，我们将探讨业余爱好和工业用途中常用的无铅焊料类型，以及用于改善其性能的掺杂剂。

## 在罐头盒里

锡(Sn)如此普遍地用于软焊料和焊料合金有一个很好的原因:它在低温(232°C)下熔化，除了能够与大多数金属很好地溶解之外，还提供良好的润湿性(在焊盘上流动的能力)。这最后一个特性对于形成良好的金属间化合物(IMC)至关重要。IMC 边界的质量决定了接头的耐用性。IMC 中任何空隙的粒度和数量(和尺寸)都会影响耐久性。

![](img/b1585bb41c5eae6226e545e69f2c316d.png)

两种最常用的无铅焊料是 SnAgCu(锡银铜，也称为 SAC)和 SnCu(锡铜)。含 3%银和 0.5%铜的 SnAgCu 合金(SAC305)最初被[认可](https://www.intechopen.com/books/recent-progress-in-soldering-materials/evolution-of-pb-free-solders)用于 SMT 组装，还有许多其他 SAC 合金。这些其他合金是含银量较高的类型，如 SAC387(含银 3.8%)和 SAC405(含银 4%)。这些高银合金是真正的共晶合金——在 217°c 的熔点下完全从固态变成液态。相比之下，SAC305 的熔点范围为 217–219°c。

虽然 SAC 是一种可接受的焊料合金，但是银的加入确实提高了它的成本。这促使该行业使用低银合金(如 SAC0307)或无银替代品，如 SnCuNi。

## 回到国际媒体委员会

可靠接合的关键在于所施加的 IMC 的质量。它不能太厚或太细，最好不要有任何[kirkendal 空隙](https://en.wikipedia.org/wiki/Kirkendall_effect)。

每个关节的 IMC 受到各种类型的老化和损伤:

*   热循环
*   热冲击
*   跌落冲击
*   震动
*   电迁移

其中，热循环和[热冲击与](https://en.wikipedia.org/wiki/Thermal_shock)相关，因为两者都是由环境温度引起的。当接头暴露在不断变化的温度下时，其单个部件将受到热膨胀的影响，这在不同材料之间可能是不同的。接头的[抗拉强度](https://en.wikipedia.org/wiki/Tensile_strength)决定了在哪个点上产生的应变会导致裂纹的形成。

通常，在热循环下，IMC 会发生再结晶，导致 IMC 变粗糙，从而形成裂纹。[研究表明](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6735330/?report=classic)添加 La [2] O [3] 纳米颗粒提高了热可靠性，主要是通过抑制 IMC 的生长。高银合金也表现出更好的热可靠性。向低银合金中添加 0.1%的铝(Al)也有这种效果，向 SnAgCu 合金中添加 Ni、Mn 和 Bi 也有这种效果。

![](img/615d3a04611bef44a4a6f4e51da2962a.png)

Drop impact crack path of test boards in the IMC.

跌落冲击和振动也有类似的关系，会产生某种机械变形，从而影响 PCB、接头和元件。特别是对于大引脚数的 BGA 芯片，跌落冲击会导致显著的损坏，测试诸如接头的剪切强度之类的特性。机械振动的失效模式类似于热循环的失效模式，由裂纹的逐渐发展引起。

![](img/e0b40a78bea102e9f56d94bd9d5ac06e.png)

Electromigration failure of interconnected solder joints.

最后，[电迁移](https://en.wikipedia.org/wiki/Electromigration)是最阴险的，因为它不需要任何外部影响。电迁移的最终效应是在电子和扩散的金属原子转移动量时，由离子的逐渐运动引起的材料在接头和 IMC 内的迁移。阳极和阴极之间的接头内的电流导致空穴的形成。随着时间的推移，这些空隙变得足够大，以至于在接头和 IMC 中形成裂纹，直到接头最终失效。在更高的温度和电流下，这一过程加速。

[防止电迁移](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6735330/?report=classic)包括调节温度和电流密度，以及调整焊点的成分和结构，以提高其抗电迁移能力。添加钴(Co)显示出改善了抗电迁移性，添加镍(Ni)和铋(Bi)也是如此，后者还降低了合金的熔点。两者似乎都通过抑制 IMC 的生长来提高抗电迁移性，这似乎是一个关键因素。

## 更少的合金

在 70 年代、80 年代和 90 年代的大部分时间里，几乎所有的焊接都是在相对较大的焊盘上完成的。大部分(如果不是全部)涉及使用 DIP 封装或类似封装的通孔焊接。随着表面贴装焊接和使用更小的封装(如 SOIC、TSSOP、QFN 和 BGA)变得普遍，随着焊盘变得越来越小，IMC 的[强度及其耐用性变得越来越成问题。](https://www.tandfonline.com/doi/full/10.1080/14686996.2019.1640072)

正如我们之前看到的，电迁移是一个主要问题，它与热弹性和机械弹性一起在现在和未来都将发挥重要作用。这些问题的解决方案将决定我们设备的使用寿命，以及新智能手机的掉落是否只是一件麻烦事，还是会破坏 0.2 毫米间距 BGA 封装上的六个微小焊球。

## 输入 SN100C

![](img/933f936dc0b16522fae595737e85196d.png)

Roll of SN100C alloy.

虽然 SnCu as 合金不是焊接的首选，因为铜往往会形成相当粗糙和易碎的 IMC，但一种可以与 SnPb 和 SAC 合金竞争或超过它们的微合金变体[自 90 年代以来一直存在，当时](http://nihonsuperior.co.jp/english/wp-content/themes/nihonsuperior/pdf/technicalinfo/tech_english12.pdf) [Nihon Superior](http://nihonsuperior.co.jp/english/product/leadfree/) 开发了 SN100C，即 SnCuNiGe。不幸的是，这种合金直到最近还受到专利保护。它的熔点为 227°C，其中 0.05%的镍促进了有光泽的接头，同时降低了铜焊盘的腐蚀。0.009%的 Ge 促进润湿并防止浮渣的形成。

由于这种共晶合金比 SnCuAg 合金更便宜，并且其[更好的属性](https://fctsolder.com/wp-content/uploads/2017/03/SN100C.pdf) [例如返工](https://www.researchgate.net/publication/266870017_Comparison_of_Copper_Erosion_at_Plated_Through-Hole_Knees_in_Motherboards_Using_SAC305_and_an_SnCuNiGe_Alternative_Alloy_for_Wave_Soldering_and_Mini-pot_Rework)，它似乎是专业人士和业余爱好者的一个有趣的选择。随着专利到期(但“SN100C”仍是商标)，许多制造商现在已经将这种合金添加到他们的目录中，包括[亚锡尔](https://www.stannol.de/en/news/new-products/sn100c/)和[费尔德](https://www.felder.de/products/electronic-applications/wave-soldering-selective-soldering/nige-solder-sn100ni-snag-sn100c/elektroniklot-iso-tin-sn100ni-5512941026.html) (Sn100Ni+)，使其更容易获得。

## 材料科学是关于妥协的

焊料合金的核心是材料科学领域，根据定义，这是一个折衷的领域。提高一个方面的质量，降低另一方面的质量。当我们考虑使用微合金化来提高 IMC 的机械稳定性时，我们可以看到这一点，从而导致更差的抗电迁移性等。

有时，有人会说我们已经找到了使用 63/37 SnPb 焊料的完美焊接合金，但随着电子产品的不断小型化和软焊接合金研究的不断进步，我们可以看到出现了许多要求，这些要求在 20 世纪 90 年代甚至都不是问题，但现在我们可以应用新知识来解决这些问题。通读 2005 年关于这个主题的科学论文与今天的对比，确实显示了我们已经走了多远。

锡最令人讨厌的特性之一——锡须——仍然是最难完全解决的问题之一。虽然铅确实抑制了锡须的发展和生长，但这并不是一个完美的解决方案。在这一点上，SnCuNiGe 等合金似乎在这方面提供了相当的性能，并已被推荐为插入式解决方案。

## 制造更好的合金

随着不断收缩的焊点的热循环和剪切强度等问题成为一个问题，我们用来组装 PCB 的合金的精炼是一个值得解决的问题。如果我们能够使 500+铅 BGA 封装的组装及其超过 10 年的日常使用可靠性成为一种近乎确定的事情，那么这意味着需要回收或最终被填埋的电子废物将会减少。

同样，为爱好者提供更容易使用和更可靠的合金也越来越成为一个话题。爱好者不再只是将几个 74 系列 DIP ICs 塞进一个通孔电路板。我们更经常看到 QFN、TSSOP 和类似的封装被使用。随着新合金润湿性的提高和桥接电位的降低，它将使每个人的生活变得更好。