# 使用 PCB 对 PCB 进行回流焊–花 2！

> 原文：<https://hackaday.com/2021/10/06/using-a-pcb-to-reflow-pcbs-take-2/>

让你的电子项目升温并不是太难。将走线设计得过小，不小心将电池输入端短路在一起，可能会使进入 MCU 的电压反向。这些年来我们都做过一两部分。但是制造一个故意变热的 PCB 会怎么样呢？这正是[Carl Bugeja]在他的 PCB 热板第二次修订中所做的，旨在回流其他 PCB。

[卡尔]第一次尝试做热板，结果不冷不热。电路板是铝基板顶部的一条蜿蜒的轨迹，它确实像预期的那样变热了。然而，薄基板导致热板在加热时严重翘曲，减少了与被焊接电路板的接触。最重要的是，阻力比预期的大得多，导致热量输出低得多。

新版电路板的基板更厚，走线更粗，电阻从之前设计的 36 欧姆降至 1 欧姆。更厚的基板，搭配更少插槽的新设计，使表面更加坚固，受热时不会弯曲。

我们尤其喜欢[Paul]为他的新电热板提出的布线解决方案。焊接到电阻加热器可能是一个巨大的烦恼，因为电路板将充当散热器。虽然鳄鱼夹确实可以用于测试，但它们之间总有滑动和短路的可能。[Paul]决定制作一个定制的柔性 PCB，用尼龙螺丝连接到电热板，并直接安装到他的电源连接点上。

不幸的是，这个新的修订版也有一些问题。其中最大的问题是与电路板制造商沟通不畅，所用的阻焊膜在工作温度下几个小时后开始退化。但对于轻型工作和间歇使用，它是完美的工具。

在我们之前的[报道中，你可以在这里](https://hackaday.com/2021/03/21/pcb-reflow-with-a-pcb/)读到更多关于【Paul 的】第一个 PCB 热板的信息。

 [https://www.youtube.com/embed/ZChSbpBbrt4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZChSbpBbrt4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

