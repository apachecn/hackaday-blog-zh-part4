# 无单片机风扇控制器

> 原文：<https://hackaday.com/2021/12/31/the-no-mcu-fan-controller/>

2019 年，这里任何控制项目的默认设置都是触及微控制器。它们的成本如此之低，无处不在，以至于可以用最少的部件来复制曾经可能需要一些额外电路的东西。但我们现在是在 2021 年底，当然，在半导体短缺的情况下，微控制器很难得到。[Hesam Moshiri]有一个项目将我们带回到一个更简单的时代，[一个温控风扇，就像它们过去被制造的那样，没有微控制器的存在](https://hackaday.io/project/183296-cooling-fan-controller-using-an-lm35-no-mcu)。

老手无疑会猜测这种设计的方向，有一个 LM35 温度传感器产生与其温度成比例的电压，还有一半的 LM358 形成一个比较器，用于比较来自分压器的静态电压。LM358 的输出驱动一个 MOSFET，该 MOSFET 反过来打开或关闭风扇电机。这种类型的电路曾经是简单控制电子产品的日常费用，当时微控制器代表着一笔巨大的费用，现在仍然是一个方便的电路。

在车载传感器的世界里，你忘记了 LM35 这样的传感器吗？[刷新你的感应记忆的时间](https://hackaday.com/2021/02/19/practical-sensors-the-many-ways-we-measure-heat-electronically/)。