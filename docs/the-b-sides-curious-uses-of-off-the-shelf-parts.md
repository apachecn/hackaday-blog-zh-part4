# B 面:现成零件的奇怪用途

> 原文：<https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/>

我承认:几年没有方便的机械车间的原型制作确实磨砺了我车削金属芯片的味蕾。但是，远离合适的机床的所有时间也促使我重新想象零件目录，这是我几乎每天都会看到的东西。手边没有任何精密金属加工工具，库存机械零件成了我对复杂性的补充。因此，以前那种让一切都由你自己来加工的教条，已经转变成了寻找那种已经为你做好准备的部件。

但是由于零件目录中有成千上万专门制造的零件，我开始重新想象其中一些零件的其他罪行。在花了几年时间为这些部分重新发明用例之后，我准备告诉你如何正确地误用它们。所以今天我想向你展示一些我最喜欢的机械零件 *B 面*，可以这么说。这些都是非传统领域的普通器件，你肯定不会在数据手册中找到！现在让我们来看看。

## 从钢球和销到运动联轴器

为了热身，让我们从运动耦合开始。运动耦合是一种机械设计模式，当应用于两个组件时，允许这些组件以极高的*重复性*连接和断开。这个性质来自于遵循[精确约束](https://hackaday.com/2019/09/11/books-you-should-read-exact-constraint-machine-design-using-kinematic-principles/)的方法。根据设计，这两个组件在每个自由度上都有一个约束连接在一起，不多也不少。结果是，当连接在一起时，耦合的部分既不会束缚也不会摆动；它们以唯一的方式组合在一起。

运动学耦合通常[用于光学仪器设置](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_id=1546)中，在这种情况下，镜子和透镜需要在没有束缚或摆动的情况下进行微调。通常情况下，这些联轴器由非常致密的材料制成，如硬化钢，这样联轴器的接触点不会变形。这对于 Thorlabs 来说可能很好，但我们也可以从库存和 3D 打印零件的大杂烩中制作一些像样的麦克斯韦耦合。

[![](img/06b0d69dc72e8de5020da239b5a0997c.png)](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/44072618500_0fc2bea4d2_k/)

An early kinematic coupling proof of concept.

[![](img/cebd3b9847fa3825873e693ca4451785.png)](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/45993844664_86867995d0_k/)

an assembled subsection of a cnc pen plotter.

[![](img/a0f50c19c67df55ac87db3d4e77d9a65.png)](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/39856650733_dff6e444fa_k/)

The toolchanging pen plotter’s carriage

[![](img/ae2b081a1a83220e5902216f3c32ceca.png)](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/40356384963_91a4428fae_k-2/)

and a rack full of pen tools.

在这种设置中，联轴器中的六个接触点由硬钢零件制成，就像它们昂贵的对应零件一样，但其他所有东西都是 3D 打印的。由于这种设计中的高应力点被密集的组件所覆盖，因此结果在大部分是 3D 打印的同时具有相当高的可重复性。事实上，在测试上面的耦合时，我观察到一致的可重复性在 25 微米以下。当然，这可能超过了一些高端耦合的亚微米可重复性，但对于许多应用来说，这是非常棒的。

我试验过类似上面的设置，混合了压配合定位销或带肩螺钉与螺纹钢球。定位销和带肩螺钉在 McMaster-Carr 或 Aliexpress 上可以很快找到，但螺纹球实际上是 Kossel Delta 3D 打印机的 [3D 打印机替换零件](https://www.aliexpress.com/item/32646556334.html)。不言而喻，我们对库存零件的偏好不一定仅限于零部件目录，而是可以扩展到 RC、3D 打印机和其他爱好者替换零件的生态系统，这些零件现在已经被它们所涉及的消费品商品化了。

## 为固定而重铸的电池夹

现在让我们将精确定位的冒险从光学实验室转移到湿实验室，在那里我们发现自己正在使用 96 孔板。在自动化设置中，这些板将被固定到机器甲板上，在那里高架机器人将对它们进行液体转移。在这里，盘子需要握得足够紧，这样它们就不会随着机器的振动而移动——但不能太紧——否则当科学家到达现场收集它们时，它们会有溢出的风险。

在这里，将这些孔板保持在固定位置的温和预载是理想的。某种钢板弹簧会很好，但是定制的钢板弹簧很贵。所以让我们问:另一个提供所有形状和大小的温和预载的规范部分是什么？当然是电池夹！

[![](img/4ed6e3ecb36c8ef9ee8255aa5eb03edb.png)](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/img_20200822_153713/)

Battery Clips keep plates in place.

[![](img/7d0325424ac7781b5943757f85b80983.png)](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/img_20200822_153553/)

The full deck region

[![](img/dcecc46ea02fc9f060af09b02308536e.png)](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/img_20200822_154138/)

of a homebrew sonication station.

在这里，我选择了 Keystone Electronics 的 5205 电池接触弹簧( [Digikey](https://www.digikey.com/product-detail/en/keystone-electronics/5205/36-5205-ND/2745874) )，用于模制塑料。我的设置导致它们被压入三层堆叠的激光切割 Delrin 中，没有任何电池，但是嘘——接触者永远不会知道区别！由于电池触点被设计为长时间压缩而不会疲劳，触点不应该在一夜之间从夹具中的板变弱。(没有说明它们的额定周期数，但对于一个预算原型来说，这些就足够了。)

## 预算有限的迷你弹簧锚

现在让我们过渡到使用拉伸弹簧。这些弹簧通常在两端都带有环，以便更容易连接到目标应用中。但是当要将它们连接到 3D 打印或激光切割的塑料部件上时，将弹簧连接到小型集成塑料部件上有可能会撕裂部件。

一种解决方案是一种叫做*弹簧钩*或*弹簧锚*的库存零件。虽然大型弹簧锚往往是多产的，但小型的却不是。唉，在我最初寻找弹簧锚的时候，我只能在我寻找的 M3 音阶中找到[一个 Misumi 部分](https://us.misumi-ec.com/vona2/detail/110300266730/?HissuCode=ASPO3-10)。每个 5 美元，比我的紧固件桶里的其他库存零件贵得多。至于在这种情况下简单地选择螺钉，结果是它们造成了不方便的弹簧锚，原因有两个:(1)头部妨碍了弹簧的安装，以及(2)只有当拉伸弹簧可以垂直于螺钉安装时，它们才能很好地工作。我想，在这一堆零件目录中，肯定有更便宜的解决方案。

 [![Keystone PN: 4000 yields to the Pliers!](img/29b4f0b814a829ae5979c404bf123535.png "bed_spring_bend_1")](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/bed_spring_bend_1/) Keystone PN: 4000 yields to the Pliers! [![An extension spring looped between two terminal lugs](img/9fc5cc8c9bfa409e4e86802a39fdb586.png "bed_spring_bend_9")](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/bed_spring_bend_9/) An extension spring looped between two terminal lugs [![Jubilee's Bed Springs. Image Credit: [Cindy Feng]!](img/6e2f880a026bec991fb8e22c06a0e5a6.png "z_coupler_spring_installation")](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/z_coupler_spring_installation/) Jubilee’s Bed Springs. Image Credit: [Cindy Feng]! [![Keystone PN: 7328 also yields to the pliers!](img/d23141dc00f85d8f80512ea5ded93d71.png "spring_anchor_formation")](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/spring_anchor_formation/) Keystone PN: 7328 also yields to the pliers! [![PN: 7328 post bending operation](img/3518ee2a8aa2508388489befa483f81a.png "formed_spring_anchor")](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/formed_spring_anchor/) PN: 7328 post bending operation [![Springs installed in a Series-Elastic Actuator](img/d0d0b1bb0cf16c7b07c3e48f17b0efc4.png "IMG_20200501_132326")](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/img_20200501_132326/) Springs installed in a Series-Elastic Actuator

确实有！答案以*焊接接线片*的形式出现。这些通常用于在一端焊接到电线上，在另一端拧入电端子。每个大约 20 美分，也很便宜。最重要的是，由于它们是由黄铜制成的，所以可以用钳子将它们加工成便于将弹簧保持在特定方向的形状。我已经使用了 Keystone Electronics 的 7328 ( [Digikey](https://www.digikey.com/product-detail/en/keystone-electronics/7328/36-7328-ND/316697) )和 4000 ( [Digikey](https://www.digikey.com/product-detail/en/keystone-electronics/4000/36-4000-ND/316071) )零件，在紧凑的奇怪配置中钻孔小拉伸弹簧，每个弹簧首先被轻轻地“折叠”到方便的方向。

## 排气螺钉被重新想象成电缆张紧器

这些接下来的部分回想起我的 [3 部分迷你系列建立两阶段电子触手机制](https://hackaday.com/2016/09/13/the-bootup-guide-to-homebrew-two-stage-tentacle-mechanisms/)。这些系统由一对手动控制器驱动，手动控制器拉动一组机械控制电缆。就像自行车一样，将这些电缆调整到合适的张力是让它们平稳工作而没有任何可察觉的“溢出”或*反冲*的关键。自行车依靠一种基于螺钉的机构，该机构允许用户通过有效地改变线缆外壳的长度来微调张力。我可以用库存零件做同样的事情吗？

是啊！事实证明，我已经盯着麦克马斯特-卡尔的 [*通风螺钉*](https://www.mcmaster.com/screws/system-of-measurement~metric/socket-head-screws/vented-socket-head-screws-6/thread-size~m3/) 类别好几年了，希望有一天我有理由买它们，这一时刻终于到来了。通风螺钉本质上是在中心钻一个小孔的螺钉。如果我是某个专门研究压力容器的工艺工程师，我可能会告诉你这些螺钉与 o 形圈结合在一起是如何构成伺服压力控制系统的有用部分的。但是我不能。我*可以*告诉你的是，将机械控制电缆穿过这些通风螺钉会产生一个特殊的电缆张力调节点。

[![](img/7341c90ae748866e73901d21a3be742f.png)](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/img_20181029_214908/)

This screw has a hole down the middle!

[![](img/79788c031d72b38acf9f56633703c8c0.png)](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/img_20181029_214734/)

Twisting the screw increases cable tension!

通过在激光切割控制器的每根电缆上安装一个通风螺丝，整个系统可以进行微调，以获得高保真的木偶表演，就像 1979 年的外星人胸部爆炸场景一样引人注目。

## 对峙三明治

支架是两端都有螺纹的金属柱。它们可能是电子工程师安装电路板的必备工具，但我认为它们是在快速原型制作或业余爱好者用例中安装 m *任何*大部分扁平元件(不仅仅是电路板)的绝佳方式。我把这种技术称为*僵持三明治*，在之前我已经[提到过一次。在这里，支架与激光切割元素相结合，构建出一个 3D 结构。由于它们有多种长度可供选择，我们只需购买正确长度的零件，从而避免了按长度加工零件的需要。我们也不需要把自己局限在一层。双层和三层三明治都是公平的游戏。每个大约 50 美分，相当大一部分建筑的总成本也相当便宜。](https://hackaday.com/2019/02/08/eight-years-of-partmaking-a-love-story-for-parts/)

 [![Odds and Ends on my 60W Laser Cutter](img/3431da63664f0cb42e9fb81a080eb12e.png "30680747325_b1d6228caf_c")](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/30680747325_b1d6228caf_c/) Odds and Ends on my 60W Laser Cutter [![Details on an old Laser-Cut CoreXY](img/843e949fd40f183c68a3cfb5b82660b3.png "16312338077_83ebfe94b2_c")](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/16312338077_83ebfe94b2_c/) Details on an old Laser-Cut CoreXY [![Gamecube-Bot 2](img/363b28d049abf22c5749daf07c882f5f.png "gamecube-bot-standoff-sandwich")](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/gamecube-bot-standoff-sandwich/) Gamecube-Bot 2 [![Gamecube-Bot 3 Prototype](img/75a75d444d254491b8e8a35c2057e6ea.png "21776453222_7f4d8ea4a8_c")](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/21776453222_7f4d8ea4a8_c/) Gamecube-Bot 3 Prototype [![Motorized Tentacle Prototype](img/3c68840f5be4ed5944b0a92d39c5c111.png "IMG_9785")](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/img_9785/) Motorized Tentacle Prototype [![... uses standoff-sandwiches to the extreme](img/c30f8032a7ffa05868775c458d50ee17.png "IMG_9788")](https://hackaday.com/2020/09/02/the-b-sides-curious-uses-of-off-the-shelf-parts/img_9788/) … uses standoff-sandwiches to the extreme

最近，我发现当与 3D 打印或激光切割零件混合时，它们对小规模机器人应用很有用。

## 零件词汇表

两年前，我拆掉了车库里的“机械车间”，然后重返校园，完成最后一项任务。当我最好的工具沉睡在仓库里时，我想我会放弃用源源不断的机械加工项目来喂养我饥渴的灵魂。

但是发生了别的事情。在远离工具的地方，我找到了零件目录。这些“挑选部分土地”的实地指南成了我的救命恩人，一种设计部件的新方法——不需要实际加工任何东西！通过一些创造性的用例重新想象，我发现这部分词汇的能力远远超出了书本上所说的。通过今天的例子，我希望你也开始明白这一点。所以下一次你需要一个小机器商店“胶水逻辑”，我希望你挑战自己，超越你能做的，并包括你能找到的跨度。