# 向 DIY 金属 3D 打印机进军

> 原文：<https://hackaday.com/2019/07/26/the-march-toward-a-diy-metal-3d-printer/>

[海纳]花了 7 年时间研究电子显微镜，花了 5 年时间研究 3D 打印机。现在的目标是将两个领域的专业知识结合到基于电子束熔化的金属 3D 打印机中。这个概念是一种集电子束焊机、FDM 3D 打印机和电子显微镜于一体的设备。在高真空下，电子束将被用来熔化金属(金属丝或粉末)来一层一层地建造物体。这个最终目标仍在未来，但[海纳]已经在真空室和高压系统方面取得了重大进展。

该装置围绕由 80/20 挤压铝框架制成的结构建造。主平台展示了一个电子枪，装在一个玻璃罐中，玻璃罐进一步装在一个金属网内，以防止玻璃在内爆的情况下扩散太远。

 [![Vacuum chamber enclosed in mesh (new gasket shown)](img/0db7db15fe95e74819273c04b5256b8b.png "hyna_wire_cage")](https://hackaday.com/2019/07/26/the-march-toward-a-diy-metal-3d-printer/hyna2/) Vacuum chamber enclosed in mesh (new gasket shown) [![Mold for making silicone gasket](img/8b52f34ad9a076af58b3236f671fa83f.png "hyna_vacuum_mold")](https://hackaday.com/2019/07/26/the-march-toward-a-diy-metal-3d-printer/hyna3/) Mold for making silicone gasket

家酿高压电源的设计包括一个隔离变压器(设计为 60kV)，使用半桥拓扑结构来防止高漏电感。变压器连接到降压转换器，用于灯丝加热和升压。系统的电源还连接到电压转换器，该转换器可以是电流馈电或电压馈电的，以作为电子束焊机或扫描电子显微镜(SEM)工作。在操作过程中，电源连接到 24V 输入，并通过 Wehnelt 圆柱体传送电子束，Wehnelt 圆柱体是与阳极相对的电极，用于聚焦和控制电子束。整个系统目前由 FPGA 和 STM32 驱动。

真空外壳本身已经很久了。[Hyna]铣出一个电路板，该电路板具有两个输出，用于连接 230V 预真空泵和 230V 预真空泵阀门的固态继电器(SSR ),两个输出，用于通风阀，来自 Piranni 真空计和冷阴极真空计的输入，以及用于 TMP 控制器的端口。在布拉格的 Maker Faire 演示了这个项目后，[海纳]回去铣了一个硅胶垫圈的模具，这是一个更好的电子束真空密封。

虽然我们已经听说了很多不同的金属 3D 打印方法，但这是我们第一次看到工业以外的 EBM 项目。这可能是第一次尝试将高压电子束的三种不同用途结合到同一个建筑中。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)