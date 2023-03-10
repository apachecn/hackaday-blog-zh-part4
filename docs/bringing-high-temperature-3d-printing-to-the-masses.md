# 将高温 3D 打印带给大众

> 原文：<https://hackaday.com/2020/10/28/bringing-high-temperature-3d-printing-to-the-masses/>

尽管可以在消费级桌面 3D 打印机上打印的热塑性塑料种类繁多，但最常用的细丝是聚乳酸(PLA)。这是因为它不仅是最便宜的材料，而且最容易加工。PLA 可以在低至 180°C 的温度下挤出，即使没有加热床也有可能获得良好的结果。不利的一面是，用 PLA 打印的物体往往有些易碎，而且耐热性较低。对于原型和轻型项目来说，这是一种很好的塑料，但对于许多用户来说，用不了多久就会超出它的能力。

下一步通常是聚对苯二甲酸乙二醇酯(PETG)。这种材料并不比 PLA 更难加工，但更耐用，可以承受更高的温度，通常更适合机械零件。如果你需要比 PETG 提供的更好的耐用性或更高的耐热性，你可以选择丙烯腈-丁二烯-苯乙烯共聚物(ABS)、聚碳酸酯(PC)或尼龙。但这就是事情开始变得棘手的地方。不仅这些材料的挤压温度高于 250°C，而且为了获得最佳效果，通常推荐使用封闭的印刷室。这使得他们处于业余爱好者群体通常能够处理的高端。

[![](img/1fee1e4e6021e956b7d5ca2cb058744f.png)](https://hackaday.com/wp-content/uploads/2020/10/hightemp3d_apium.jpg)

Industrial 3D printers like the Apium P220 start at $30,000.

但是高端工业 3D 打印机可以使用更强的塑料，如聚醚酰亚胺(PEI)或聚芳醚酮家族的成员(PAEK，PEEK，PEKK)。由这些材料制成的部件对于航空航天应用来说是特别理想的，因为它们可以代替金属部件，同时重量大大减轻。

这些塑料必须在接近 400°C 的温度下挤出，并且在印刷过程中绝对需要一个保持在 100°C 以上的密封成型室。具有这些功能的商业打印机的购买价格甚至在低端也是数万美元，有些型号的价格高达六位数。

当然，曾几何时，也就是不久前，3D 打印机也是如此。机器曾经是资金雄厚的 R&D 实验室的唯一领地，现在却坐在全世界黑客和制造商的工作台上。虽然很难说我们是否会看到高温 3D 打印机的同样竞争，但这项技术民主化的第一步已经迈出。

## 工程挑战

简而言之，支持这些所谓工程塑料的机器需要是传统 3D 打印机和烤箱的融合。当然，这就是问题所在。打印机本身，尤其是我们在桌面上已经习惯的类型和质量，将无法在这样的环境中生存。对于要成功生产 PEI 和 PEEK 零件的消费型 3D 打印机来说，它需要进行大量的修改；[这正是美国宇航局在 2016 年用 LulzBot TAZ 4 做的事情](https://ntrs.nasa.gov/citations/20170000214)。

[![](img/e0d4907162b81fa7ef8bafe535afc600.png)](https://hackaday.com/wp-content/uploads/2020/10/hightemp3d_taz4.jpg)

LulzBot TAZ 4 modified for high temperature printing.

第一步是建造一个可以安装在 TAZ 4 周围的隔热外壳，并在其中安装一组 35 瓦的红外加热灯。在这种环境下，机器暴露在外的电子元件自然会过热，因此必须将它们重新放置在盒子外面。

步进电机也会过热，但兰利研究中心的团队没有试图移动它们，而是选择设计冷却外套，安装在每个电机上，加压空气可以通过它循环。

与其他桌面 3D 打印机一样，TAZ 4 在其构造中也使用了许多打印部件。这些零件印在 ABS 上，在用来支撑 PEEK 的加热室内会很快失效。这些零件是用 PC 重印的，但即使是这种材料也没有足够的弹性永久使用。因此，按照经典的 RepRap 传统，该团队在改装的打印机上以 PEI 的形式打印了第三组也是最后一组零件，商业上称为 Ultem。

有点令人惊讶的是，该团队在升级 TAZ 4 时几乎没有遇到任何问题，它的 hotend 和喷嘴可以在高达 400°c 的温度下挤出塑料。流行的 E3D-v6 hotend 价格不到 100 美元，并被发现能够达到这些温度，尽管该团队确实需要用更高额定值的型号替换其热敏电阻，并对打印机的 Marlin 固件进行一些调整，以使其达到在正常情况下会触发热关机的温度。

[![](img/7541d1d6939a7f61ec903e836de0400b.png)](https://hackaday.com/wp-content/uploads/2020/10/hightemp3d_nasaprints.jpg)

Objects printed in Ultem 1010 on NASA’s modified LulzBot TAZ 4.

最终，美国宇航局的报告得出结论，对 LulzBot TAZ 4 的改造取得了圆满成功。他们指出，试图在红外加热灯关闭的情况下印刷 PEI 会导致严重的印刷问题，如翘曲和分层，尽管这是可以预料的。没有给出改造成本的最终美元数字，但考虑到 TAZ 4 当时的基础价格约为 2200 美元，整个项目的成本可能是同类商业产品的 1/10。

## 从头开始

美国宇航局的实验表明，修改现有的开源桌面 3D 打印机来打印高温工程塑料是可能的，他们甚至表明这可以相对经济地完成。但是没有人会说这样的自举是一个理想的解决方案。在转换过程中有太多的重复工作，因为工程师们不得不专门撤销最初由 LulzBot 做出的设计选择。即便如此，这个实验确实为其他想要从头开始的项目创造了一个有价值的基线。

就在上个月，[密歇根理工大学的一个团队发布了 Cerberus](https://www.sciencedirect.com/science/article/pii/S2468067220300390) ，这是一款开源高温 3D 打印机，能够在 PEI 和 PEKK 生产零件，制造成本仅为 1000 美元。该团队没有尝试修改现有的设计，而是从头开始考虑高温打印。所有敏感的电子元件都安装在远离密封建造室的地方，该建造室使用一个由电源供电的 1 kW 空间加热器芯来快速将其加热到工作温度。

至关重要的是，所有的步进电机也被移出了建造室。虽然这确实使运动学比你在传统的桌面 3D 打印机中看到的更加复杂，但这意味着 Cerberus 不需要像 NASA 的改良 TAZ 那样的专用电机冷却系统。

 [![hightemp3d_cerberus1](img/8f6a05edc724217b2c4be250fd63f104.png "hightemp3d_cerberus1")](https://hackaday.com/2020/10/28/bringing-high-temperature-3d-printing-to-the-masses/hightemp3d_cerberus1/)  [![hightemp3d_cerberus4](img/717f56c455a12c7dfa86def5f1c7822e.png "hightemp3d_cerberus4")](https://hackaday.com/2020/10/28/bringing-high-temperature-3d-printing-to-the-masses/hightemp3d_cerberus4/)  [![hightemp3d_cerberus2](img/6b317db16db87d14f0ffed8218259152.png "hightemp3d_cerberus2")](https://hackaday.com/2020/10/28/bringing-high-temperature-3d-printing-to-the-masses/hightemp3d_cerberus2/)  [![hightemp3d_cerberus3](img/6e8ab94d93f0e19d38438b62ba9f88fc.png "hightemp3d_cerberus3")](https://hackaday.com/2020/10/28/bringing-high-temperature-3d-printing-to-the-masses/hightemp3d_cerberus3/) 

简化的设计结合使用现成的控制电子设备，包括 Arduino Mega 2560 和 RAMPS 1.4 板，以及在改进的 TAZ 4 上使用的相同的 E3D-v6 hotend，使 Cerberus 完全在有动机的爱好者的手段之内。特别是因为该团队为他们的打印机提供了清晰而详细的组装说明，这是美国宇航局的报告中明显缺少的东西。

## 扩展可能性

在美国宇航局的 TAZ 4 改型和 Cerberus 等全新设计之间，很明显，在家庭工作室打印 PEI 和 PEEK 对象的技术能力对任何人来说都是足够迫切的。这还不像在亚马逊上购买一台 200 美元的 3D 打印机那么容易，但如果有需求，更多基于这些核心原则的低成本机器肯定会开始进入市场。这与最近几年占领创客空间的当前一波廉价激光切割机没有太大区别。

[![](img/9f5998aa1fcab189671c3e97710536ed.png)](https://hackaday.com/wp-content/uploads/2020/03/prusacovid_thumb.jpg)

Makers all over the globe have been printing PPE

那么，对它们有需求吗？去年这个时候，答案可能会有所不同。但是，随着世界仍在与新冠肺炎疫情作战，[对快速生产的个人防护装备(PPE)](https://www.youtube.com/watch?v=Lpm8fx8_17M) 有了新的需求，这是任何人都没有预料到的。

正如 Cerberus 的文档中所解释的那样，密歇根理工大学的团队受到启发，专门开发了一种负担得起的高温 3D 打印机，因为它可以用于创建能够经受住高温消毒的 PPE。该团队认为，用 PEKK 打印的口罩等物品可以长期使用，而不是一次性的。

可以重复消毒的打印部件显然还有其他潜在的医疗应用。生产这些组件的便携式低成本机器可能会在世界上无法快速获得传统供应和设备的偏远地区拯救生命。

3D 打印的批评者经常说，这些机器的核心缺点是，它们打印的零件很少足够坚固，只能用作粗略的原型。但是，当一台 1000 美元的打印机可以生产航空级材料的零件时，我们似乎比以往任何时候都更接近一场制造业革命。