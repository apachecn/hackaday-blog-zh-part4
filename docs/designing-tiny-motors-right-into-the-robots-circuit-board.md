# 在机器人的电路板上设计微型马达

> 原文：<https://hackaday.com/2019/01/01/designing-tiny-motors-right-into-the-robots-circuit-board/>

马达并不过分复杂，但这款却非常简单。Carl Bujega 一直致力于一种电机设计，这种设计严重依赖于印刷电路板(PCB)制造工艺的能力。他在 2018 年 Hackaday 超级大会上的讲话涵盖了[他如何将无刷 DC 电机和速度控制器内置到 PCB](https://www.youtube.com/watch?v=uQsO3XsqpVM) 中。休息后可以看新发布的视频。

电动机有两个主要部分:定子是静止的，而转子在轴承上旋转。电磁力被用来引起旋转运动。在这种情况下，Carl 在一个 4 层电路板(每层 6 个线圈)上将电磁铁制成线圈。通电后，会产生一个磁场，推动转子中的稀土磁体。

[![](img/269c23c1ca0fe25c32753a3abdab8818.png)](https://hackaday.com/wp-content/uploads/2018/12/pcb-motor-stator.jpg) 这里有几件事真的很有趣。首先，这些线圈通常由缠绕在铁芯上的“磁线”(非常细的漆包线)制成。相反，使用电路板既节省了物理空间，又节省了以传统方式缠绕线圈的时间和费用。第二，卡尔在设计时就考虑到了制造；你可以在图像中看到，他的电机设计非常简单，只需在 PCB 中插入一个 3 毫米的轴承，将磁铁插入塑料转子，然后将其扣合到位即可。最终目标是制造作为电路板一部分的机器人执行器。

这个想法的起源来自于卡尔对无人机设计的兴趣，事实上，他在完成他的 EE 后立即投入了一家无人机创业公司。这家公司没有持续多久，但他对有趣设计的渴望一直在持续。当考虑减少建造四轴飞行器所需的总零件时，他偶然想到了基于 PCB 的线圈的想法，并将其应用于电机设计，以及一些非常有趣的柔性 PCB 机器人设计工作，你可以在他的 [Hackaday.io](https://hackaday.io/CarlBugeja) 页面、 [YouTube](https://www.youtube.com/channel/UCdxTCCRnQgfi2vr2fZupYIQ) 和 [Twitter](https://twitter.com/BugejaCarl) 上查看这些工作。

当然，这也有一些权衡。这种电机是低转矩的，因为它使用的是空芯而不是铁芯。他在实现无传感器电子速度控制器(ESC)方面遇到了困难，因为线圈的反电动势似乎太弱了。不用担心，他增加了一个霍尔传感器，并成功设计了一个尺寸仅为 14 毫米×8 毫米的电子稳定控制系统。事实上，在这篇文章顶部的图像中，他举着 ESC 和马达！

 [https://www.youtube.com/embed/uQsO3XsqpVM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uQsO3XsqpVM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

