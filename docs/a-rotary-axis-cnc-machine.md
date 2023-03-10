# 旋转轴数控机床

> 原文：<https://hackaday.com/2018/09/24/a-rotary-axis-cnc-machine/>

有一类零件不能在标准的三轴铣床上制造，也不能用 3D 打印机或车床制造。这些零件——奇怪的螺丝、凸轮轴、奇怪的齿轮，或者只是一个带键槽(或两个键槽)的轴——实际上只能用数控机床上的旋转轴来制造。当然，你可以花几千美元为哈斯或托马克买一个旋转轴，或者你可以自己造一个。这正是[ 亚当 泽洛夫]和[ 马特 马通]在今年的纽约世界创客大会上所做的。这是 Rotomill ，一种简单的三轴数控机床，带有旋转轴，几乎任何人都可以制造。

Rotomill 的设计使用标准的现成 Makita 旋转工具作为主轴，并使用丝杠通过 NEMA 24 步进电机移动 X 和 Z 轴。A 轴——旋转钻头——通过蜗轮驱动，也由 NEMA 24 提供动力。目前，这提供了足够的能量来切割泡沫、塑料和木材，也应该足够切割铝。最后一项壮举尚未测试，但其设计足够开放，可以连接一个更强大的主轴。

这台机器的软件有点奇怪。对于大多数带旋转轴的数控机床，A 轴被视为旋转轴。对于 Rotomill，[Adam]和[Matt]正在生成 g 代码，就像它是一台普通的笛卡尔机器一样，只是有一个轴“缠绕”在自身周围。这些都是通过 Autodesk HSM 完成的，运行 GRBL 的正确配置的 Arduino 可以理解所有这些神秘的几何图形。

 [![IMG_20180922_141813](img/974923b0d917f7e8efa628e9e826202c.png "IMG_20180922_141813")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180922_141813.jpg?ssl=1)  [![IMG_20180922_141921](img/504ef4ac0f61fc384fd3736b544e9332.png "IMG_20180922_141921")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180922_141921.jpg?ssl=1)  [![IMG_20180922_141803](img/58be0aa1773909c9fa0ff2ececf912af.png "IMG_20180922_141803")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180922_141803.jpg?ssl=1)  [![IMG_20180922_141733](img/f34f13e7648c05872a4391ad9c1e7439.png "IMG_20180922_141733")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180922_141733.jpg?ssl=1)  [![IMG_20180922_141927](img/246901527c4de64b2ab7bba87ac0565a.png "IMG_20180922_141927")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180922_141927.jpg?ssl=1)  [![IMG_20180922_141837](img/ad42c620e80d57d82a25b0fb66d20092.png "IMG_20180922_141837")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180922_141837.jpg?ssl=1) 

这是一台看起来很棒的机器，它背后的人说它比任何其他带旋转轴的机器都便宜得多。这是意料之中的，因为它基本上是一个五轴轧机，两个轴被删除。尽管如此，整个项目的建造成本约为 2000 美元，一些大胆的补救措施和黑客攻击可能会使价格下降一点。