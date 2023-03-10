# 周期精确的英特尔 8088 内核，满足您所有的复古电脑需求

> 原文：<https://hackaday.com/2022/12/03/a-cycle-accurate-intel-8088-core-for-all-your-retro-pc-needs/>

世界各地的反计算机爱好者面临的一个日益突出的问题是芯片的供应。一旦一块硅停止生产，它的需求可以在一段时间内由旧库存和二手零件来供应，但随着它们变得越来越稀少，那些可疑零件的成本就会加速上升，变得遥不可及。至少对 CPU 来说，令人高兴的是，基于 FPGA 的核心有望取代真正的核心，而对于早期的 PC 用户来说，来自[Ted Fried]的一种新的核心。 [MCL86 是一款周期精确的英特尔 8088 FPGA 内核](https://hackaday.io/project/188412-mcl86-cycle-accurate-intel-8088-fpga-core)，可用于 FPGA 设计中，也可作为实际 8088 的独立在线替代产品。它甚至有一个全速模式，牺牲周期精度，可以将那些 8088 指令加速 400%。

阅读[他博客](https://microcorelabs.wordpress.com/2016/03/03/lots-of-interest-in-the-mcl86-core/)上的帖子，很明显这是一个有能力的设计，甚至还扩展了一种模式，增加了高速缓存 RAM [，以反映处理器速度](https://microcorelabs.wordpress.com/2022/07/31/mcl86-8088-accelerator-update/)下的系统内存。你可以在 GitHub 的资源库中找到所有的代码[，如果你有足够的好奇心去亲自研究的话。我们过去一直在思考 x86 单板计算机在哪里，也许像这样的项目可以提供一些 x86 单板计算机。](https://github.com/MicroCoreLabs/Projects/tree/master/MCL86)