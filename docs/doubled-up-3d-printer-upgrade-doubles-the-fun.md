# 双倍 3D 打印机升级带来双倍乐趣

> 原文：<https://hackaday.com/2022/03/17/doubled-up-3d-printer-upgrade-doubles-the-fun/>

内森在 YouTube 上制作机器人对改装 3D 打印机并不陌生，不管这是不是一个好主意，有时候发现这一点很有趣。他最近的恶作剧被他称为[双安德](https://www.youtube.com/watch?v=FHK-s3yqwek)(视频，嵌入下面)，在那里他不仅将酒店翻了一倍，而且还将其他一些地方翻了一倍。目的是实现双材料印刷，他的具体目标是在同一印刷中结合普通尼龙和碳纤维尼龙，以获得两种材料的最佳性能。

![](img/fad788e1c70d288099963f7120f31f80.png)

Perfects results on the first try!

以 Ender 3 v2 为例，[Nathan]首先安装一个双 Z 轴套件，将 Z 轴螺丝和相关的步进电机折叠起来。这可能是为了补偿后续模块的额外重量。由于股票安德主板只有一个 Z 轴端口，不太明显的解决方案是只安装第二个主板！通过利用 [Klipper 打印机固件/软件栈](https://www.klipper3d.org/)的强大黑客能力，他能够让这个奇怪的配置工作起来。

接下来是构建的主要部分；菲图斯太极双热端装置。出于某种原因，最初，我们决定将库存 bowden 注射器/挤出机与直接驱动的第二个单元结合起来，我们猜测这可以使往复重量下降一点，并让您直接比较同一台机器上的 bowden 和直接驱动打印结果。无论如何，第一个双材料印刷在几次(很快被掩盖)失败后表现得相当好，并且工作得足够好，双尼龙印刷现在可以成为一种选择。在将构建切换到双直接驱动设置后，[Nathan]发现更容易让机器更可靠地切换灯丝，当你想到鲍登管中所有额外灯丝的影响时，这是有意义的。

[内森]显然已经被烧死了(我们不都是吗？)可能是字面上的意思，由于一些中国供应商的奇怪习惯，随机分配电源极性给红/黑线对。这个解决方案，有些极端，就是简单地用一个嵌入式整流器制作定制的电力电缆。好吧，我们想这又少了一件需要担心的事情，但是当那些 PSU 黑客被展示的时候，请不要看别处！

多材料或多色 FDM 打印机的选择很多，这里有一个很酷的方法使用[伺服摆动一对 hotends 到同一点](https://hackaday.com/2020/02/26/80-dual-extrusion-kit-might-work-with-your-3d-printer/)，我们也看到了一段时间前，一种方法使用[弹簧加载摇杆](https://hackaday.com/2021/03/07/this-dual-extrusion-system-rocks/)翻转未使用的 hotends 到不需要的地方。

 [https://www.youtube.com/embed/FHK-s3yqwek?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FHK-s3yqwek?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[赞]的提示！