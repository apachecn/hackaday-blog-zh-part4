# 一只啄木鸟能啄多少木头？

> 原文：<https://hackaday.com/2019/04/27/how-much-wood-can-a-woodpecker-chuck/>

对于黑客读者来说，我们生活在一个业余爱好者工具可访问性的黄金时代，这一点可能很清楚。廉价的单板电脑可以在任何一个小区 ~~RadioShack 或者 Maplin~~ 买到。3D 打印机以不到 200 美元的价格出售完全组装好的现成产品。即使是不起眼的数控加工厂也降低了价格，尽管正如你可能预料的那样，在低端市场，情况会变得相当糟糕。就像一台廉价的 3D 打印机一样，一个廉价的工厂往往会缺少一些你认为任何合理的机器都应该具备的基本功能。如果你得到了这些小奇迹中的一个，[沙哈达·阿布巴卡尔]有一对关于基本升级的[博客帖子](https://blog.shahada.abubakar.net/post/adding-end-stops-limit-switches-to-the-3018-woodpecker-cnc-router)，你可能会想开箱即用。

我们在谈论哪些廉价的数控铣床？他们有几个名字。去年，我们自己的[【Kristina Panos】整理了一份由 Linksprite 销售的价格低得惊人的“1610”型的评论](https://hackaday.com/2018/01/16/review-linksprite-mini-cnc/)(如果你已经在考虑购买，去看看吧！).“1610”类，因其 16 厘米 x 10 厘米的床尺寸而得名，在各种各样的制造商名下相当常见。你可以找到像[Kristina]一样由 8020 制成的这种尺寸，或者由 1/4”神秘塑料切割而成的“升级”版本(在列表中通常称为胶木，但你的猜测和我们的猜测一样准确)。1610 是最小的型号，但基本上与 1810、2418 或 3018 的型号相同。每个都有一个 775 大小的主轴和一个处理步进驱动器和运行 grbl 的 PCBA。

那么问题出在哪里？首先，这些机器都没有限位开关，尽管控制器支持它们。[【sha hada】的指南](https://blog.shahada.abubakar.net/post/adding-end-stops-limit-switches-to-the-3018-woodpecker-cnc-router)有关于买什么样的、如何接线以及它们可以连接到哪里的简便说明。加上 g 代码指令发送控制器的概述，以便正确地设置和配置一切。控制器也喜欢通过串行连续驱动(尽管一些卖家似乎提供了一个单独的板来驱动它们)。如果你手边有一台电脑，这很好，但像 3D 打印机一样，将 Pi Zero 或类似的东西栓到设备上并通过网络控制它可能会很好。[【sha hada】的第二篇文章](https://blog.shahada.abubakar.net/post/adding-a-raspberry-pi-zero-w-and-cnc-js-to-the-3018-woodpecker-cnc-router)有一个安装板的链接，你可以准确地打印该设置，以及一些配置 CNC.js 驱动一切的建议。

你有这种机器吗？做过升级吗？在评论里告诉我们吧！我们一直在寻找方法来升级我们的家庭商店。