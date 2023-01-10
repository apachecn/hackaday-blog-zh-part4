# 用沙鼠取代传统的 CNC 电脑

> 原文：<https://hackaday.com/2018/12/04/replace-legacy-cnc-pcs-with-a-gerbil/>

网上有很多价格合理的激光切割机和其他数控机床，但让这些机器运转的主要障碍不是价格或零件。通常是控制器 PC，如果幸运的话，它可能运行 Windows XP 或 NT，但其中一些仍然使用 80 年代的 IBM XT 计算机。即使这些机器中的硬件在工作，也不可能得到软件，即使这样，它也将是过时的，缺乏现代计算机的特征。[进入超级沙鼠](https://awesome.tech/xt-computers-4-cnc-machining-really/)。

[Paul]找到了一个带有废弃控制器的激光切割机，但他认为有更好的方法让它重新运行。顾名思义，它使用了 [GRBL](https://github.com/grbl/grbl) ，一个 g 代码解析器和 CNC 控制器软件包，最初是为了在 8 位 AVR 微控制器上运行，但【Paul】设计的超级沙鼠是为了在 32 位 ARM 平台上运行。他还为它添加了 Z 轴控制，所以它现在比原来的软件拥有更多的自由度。

作为概念的证明，一旦他完成了超级沙鼠的建造，他就从中国订购了一台带有过时控制器的数控机床，并能够在一天内让它运行起来。作为额外的奖励，他把一切都开放了，所以如果你想使用他的控制器，就没有许可费或云存储需求。[Paul]也有这个项目的 Kickstarter 页面。希望控制器不是唯一阻止你为你的实验室获得数控机床的东西，但是如果他们有，你现在有了一个很好的解决方案，一个 [3040 或 3020 数控机床的](https://hackaday.com/2015/09/08/how-to-upgrade-a-chinese-cnc-machine/)控制器，或者任何其他你可能想要的数控机床。

[https://www.kickstarter.com/projects/2118335444/automate-anything-with-super-gerbil-cnc-gcode-cont/widget/video.html](https://www.kickstarter.com/projects/2118335444/automate-anything-with-super-gerbil-cnc-gcode-cont/widget/video.html)