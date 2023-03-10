# 用这个皮带传动挤压机驯服你的柔性细丝

> 原文：<https://hackaday.com/2022/05/25/tame-your-flexible-filaments-with-this-belt-drive-extruder/>

[适当的打印]显然喜欢推动 3D 打印材料的边界，有时这需要建立定制的 3D 打印机，或者至少是它们的商业端。柔性细丝可能有点难以处理，因为大多数挤出机都设计成用简单的滚花螺栓(或压紧辊装置)将细丝推入热端，并且由于塑料本身的刚性，只能可靠地工作。一旦你变得柔软，刚性就会降低，细丝经常会向侧面偏斜，挤压机就会堵塞。通向热端的灯丝路径越长，就越难。[双带驱动挤压机](https://www.youtube.com/watch?v=-LdFmPYItb0)(他们称之为“合适的挤压机”)用一对支撑带在两侧夹住细丝，将它引导到加热区，不允许它向侧面偏斜。挤出机主体和齿轮是树脂印刷的(但是，我们检查过——该设计也适用于 FDM 印刷),这证明了在现代打印机上进行树脂印刷确实能够保持足够的尺寸精度，允许制造机械装置，尽管有人反对！

挤出机的设计需要一点调整，因为皮带本身会偏转，但经过几次迭代添加一些导轨后，它似乎工作得相当好。当然，我们通常不会一路看到所有的失败！尽管如此，他们还是开始以合理的方式测试柔性细丝，从肖氏硬度为 93A 的最低柔性细丝开始，然后迅速转向 NinjaFlex (85A 硬度)，甚至成功地在一种未知的 60A 硬度细丝中打印出齿轮。

测试打印机是 Creality CR-10，安装了 WhamBam 突变体换刀装置，因此需要一个转接板来安装“合适的挤出机”。皮带驱动的设计，加上改装带来的额外摩擦，证明对于用于直接驱动挤出机的典型 NEMA17 步进电机来说有点太多，所以他们需要使用更强大的装置。由于这个更大的电机产生的热量，它需要印刷在聚碳酸酯上(我们认为，视频不清楚)，以防止操作过程中的翘曲，但我们认为，这应该不会成为无畏的建设者想要复制这项工作的主要障碍。

我们对使用柔性材料的 3D 打印并不陌生，也不陌生驯服它们的相关技术，比如这个[为 TPU](https://hackaday.com/2019/05/16/a-better-bowden-drive-for-floppy-filaments/) 改进的鲍登驱动器。用 flex 打印的应用很多，也很重要，比如[打印定制垫片](https://hackaday.com/2022/04/20/gaskets-can-they-be-3d-printed/)，仅举一例，所以在我们看来，任何降低用软盘打印难度的事情都是朝着正确方向迈出的一大步。

 [https://www.youtube.com/embed/-LdFmPYItb0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-LdFmPYItb0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[BaldPower]的提示！