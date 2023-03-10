# 在一个微小的外壳中构建 1.4W 激光指示器

> 原文：<https://hackaday.com/2019/02/19/building-a-1-4w-laser-pointer-in-a-tiny-housing/>

激光笔刚出来的时候很酷，只有 30 秒钟，很快就过时了，对老板的季度报告演示毫无帮助。然而，就像音箱和跑车一样，更大的功率总能让事情变得更好。[Styropyro]对他从易贝买来的又弱又不可靠的激光笔不以为然，于是他拆掉了一个，开始重新制作。

在摆弄了一些基本的 1mW 易贝绿色激光器后，[styropyro]通过摆弄内部的装饰孔来转动灯芯。这导致了廉价激光二极管的快速和不合时宜的死亡，留下了一个紧凑的激光指示器外壳，为黑客攻击做好了准备。

为了取代乏味的库存组件，[styropyro]选择了 Nichia NDG7475 高功率激光二极管，将其安装到一个小型散热器中进行散热管理。电流消耗太高，无法使用原来的开关，因此库存外壳的按钮被用来切换一个 MOSFET，该 MOSFET 将全部电流传输到激光驱动器。为了达到 1.4W 的更高输出功率，激光二极管在 2.3 安培下超规格运行。所有这些电流消耗将很快淹没标准的 AAA 电池，因此一对锂聚合物 10440 电池被替代来完成这项工作。

该产品表明，通过巧妙的零件选择和一些简单的手工焊接，你也可以在家里制作一个非常危险的激光笔，它可以整齐地放在你的衬衫口袋里。或者，你可能更喜欢大尺寸的东西。休息后的视频。

 [https://www.youtube.com/embed/7WoNWslRx1g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7WoNWslRx1g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

