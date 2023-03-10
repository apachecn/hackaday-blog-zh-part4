# 用砂纸和微焊修复工厂缺陷 IC

> 原文：<https://hackaday.com/2022/01/31/factory-defect-ic-revived-with-sandpaper-and-microsoldering/>

我们可能会面临芯片短缺，但如果你喜欢逆向工程，就永远不会缺少有趣的旧芯片可供挖掘——2513n 5×7 字符 ROM 就是这样一种芯片。[在一个探测这些](https://twitter.com/TubeTimeUS/status/1483177904515076098) (Twitter， [ThreadReader link](https://threadreaderapp.com/thread/1483177904515076098.html) )的长线程中，【TubeTime】已经意识到有两条地址线在封装内部短路了。推特上多巴胺推动的对真相的探索让他尝试让芯片工作。试图用外部 PSU 清除短路反而导致焊线弹出，ESD 二极管连接消失就是明证。

十几分钟的砂纸打磨工作导致裸芯片暴露在外，副作用是焊接线快速工作。显然，焊盘过于靠近会导致两个焊盘合并在一起的工厂缺陷。难怪 PSU 不会接受！一些 X-acto 工作后，短路被清除。但是如果没有连接线，[TubeTime]将如何连接它呢？这就是图片中的作品出现在的地方。焊接到接合线的剩余部分已被证明是卓有成效的，足以使芯片复活以继续研究，即使它似乎从未开始发挥作用。该线程继续比较[TubeTime]手头上的几个不同芯片的 rom，并推断可能发生了什么，导致 IC 在野外消失。

这样的焊接实验总是有趣的尝试和成功！我们很少看到如此小规模的焊接，谢天谢地，它并不总是需要的，但当有人做 IC 或 [PCB 显微手术来修复工厂缺陷](https://hackaday.com/2021/12/14/pcb-microsurgery-puts-the-bodges-inside-the-board/)时，这是一种快乐，这些缺陷使我们的设备在发货前就无法使用。每当一个黑客伙伴敢于磨掉集成电路环氧树脂层，并且[拯救了一个游戏控制台](https://hackaday.com/2019/03/21/a-steady-hand-makes-this-chip-work-again/)或者[一个身份不明的复杂电路板](https://hackaday.com/2017/10/15/get-down-to-the-die-level-with-this-internal-chip-repair/)，世界就会变得更加光明。如果你不是因为维修的原因而被迫这么做，你可以尝试建造现存最小的 NES！

> 这可能行不通，但值得一试。[pic.twitter.com/Lv6maiEEtC](https://t.co/Lv6maiEEtC)
> 
> —tube☃time(@ tubetimeus)[2022 年 1 月 22 日](https://twitter.com/TubeTimeUS/status/1484734718532734977?ref_src=twsrc%5Etfw)