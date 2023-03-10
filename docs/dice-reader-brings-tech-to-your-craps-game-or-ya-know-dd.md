# 骰子阅读器给你的骰子游戏带来了科技……或者，你知道，D&D

> 原文：<https://hackaday.com/2019/08/04/dice-reader-brings-tech-to-your-craps-game-or-ya-know-dd/>

你可能已经听说过一些关于骰子的老生常谈:如果你只有一个骰子，它就被称为“骰子”，每个骰子的反面总是加起来有七个，你加在一起的那些点被称为“点数”。但是那些点的红外属性呢？事实证明，它们比骰子的白色主体反射更少的红外线，这一特性可用于构建自动骰子阅读器。

[![](img/8472f96dfd427d531499e442a8bea350.png)](https://hackaday.com/wp-content/uploads/2019/08/IR-dice-reader-detail.jpg) 伟大的项目都有浮出水面的办法。这个概念的证明可以追溯到 2009 年，虽然源博客现在已经不存在了，[幸好它被互联网档案馆](https://web.archive.org/web/20100225014507/http://grathio.com/2009/08/dice-reader-version-2.html)保存了下来。在重建基于这个基本描述的项目时，[Calvin]使用了一组五个红外发射器/接收器对。仔细观察，你会发现每个发射器都隐藏在它的配套接收器下面。光线穿过接收器，通过测量反射回来的光量来检测 pip 的存在。

该板只是设计中的传感器部分。一个 595 移位寄存器提供了控制哪个 IR 对被供电的能力，另外还有五个信号输出到 Arduino Uno 的模拟引脚，以监控接收器检测到多少光。嘿，这是关于骰子的另一个有趣的事实，你只需要读取五个不同的点数来建立显示的值！

我们希望有一个演示视频来展示这一点，但可惜我们找不到。听到[Calvin]提到这是大学里的一项分类任务，我们觉得很有趣，这个团队不想再做一个糖果分类器。看，[我们和下一个电子极客一样热爱史诗般的 M & M 分类器](https://hackaday.com/2017/02/06/mms-and-skittles-sorting-machine-is-both-entertainment-and-utility/)，但是要胜过这个每天滚动 130 万次的基于骰子的随机数发生器[是相当困难的](https://hackaday.com/2009/05/26/dice-o-matic/)。