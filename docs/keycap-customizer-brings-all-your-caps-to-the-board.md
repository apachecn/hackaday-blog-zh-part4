# 键帽定制程序将您的所有键帽带到板上

> 原文：<https://hackaday.com/2020/08/15/keycap-customizer-brings-all-your-caps-to-the-board/>

明亮的颜色和复杂的设计，除了键盘的外形，最引人注目的当然是键帽。历史上，键帽由它所连接的按键开关的杆决定，键帽有各种尺寸、颜色、外形和设计。因为它们必须包括具有紧密公差的小特征以配合它们的按键开关的杆，所以注射成型是键帽的经典制造技术。但随着 3D 打印爱好者的成熟和树脂打印机变得更容易获得，家庭键帽制造越来越成为好的选择。与其手动设计每个瓶盖，不如考虑尝试[rsheldii]的 [KeyV2 OpenSCAD 脚本来轻松创建自定义瓶盖](https://github.com/rsheldiii/KeyV2)。

为了涵盖基础知识，KeyV2 可以在 SA、DSA、DCS 配置文件中生成带有 Cherry 或 Alps 字干的完整键帽集(以及更多！)用于任何典型尺寸的键盘。生成任意轮廓、位置和大小的特定 cap 只需调用一小段函数链。但是标准键帽集并不是这个工具集的亮点。

![](img/4d7c0000d45e673b782ca0cb1acadefd.png)

如果您还不是 OpenSCAD 爱好者，请访问[Brian Benchoffs] [优秀的入门指南](https://hackaday.com/2013/12/11/3d-printering-making-a-thing-with-openscad/)或[我们的其他报道](https://hackaday.com/tag/openscad/)来感受一下这个工具能做什么。OpenSCAD 的部分吸引力在于它是参数化建模的典范。它的声明性部分文件确保没有参数未定义，这非常适合 KeyV2。

所有键帽基于的根文件有[关于 *150* 键帽参数](https://github.com/rsheldiii/KeyV2/blob/master/src/settings.scad)可以调整，这是在更精细的定制之前。制作简单的“工匠”帽轻而易举，因为 OpenSCAD 的魔力意味着用户可以在完全参数化的键帽上执行他们需要的任何布尔运算。将任意模型与键帽相结合只需一步之遥。有关示例，请参见自述文件。

对于担心复杂性的 KeyV2 的潜在用户；别紧张，文档是一种享受。生成标准键帽的基本用法很简单，并且有大量带注释的源文件和示例来简化更复杂的用法。在考虑新键盘吗？看看我们最近的快速报道。