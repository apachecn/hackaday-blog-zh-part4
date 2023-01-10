# LED 化吉他，第二部分

> 原文：<https://hackaday.com/2018/11/23/led-ifying-a-guitar-part-two/>

电吉他是关于舞台表现力的。需要比单把吉他更酷？没问题——有双颈吉他。需要比那更酷吗？没问题，廉价魔术的家伙有一把五颈吉他。需要比那更酷吗？罗比·罗伯逊在最后一首圆舞曲中用多了一个曼陀林琴颈的吉他演奏。你从那里去哪里？显然，解决方案是在你的吉他里放一台电视，在吉他里放一大堆可单独寻址的发光二极管。这就是[Englandsaurus]正在做的事情，现在的构建思路是如何将一束 led 变成显示器。

![](img/05f826c2753a343f706a5c1db1ba6eb7.png)在[这个构建线程](https://hackaday.com/2018/09/01/led-ifying-a-guitar/)的第一部分中，【英格兰龙】讲述了吉他本身的构造，以及一百个可单独寻址的 RGB 发光二极管是如何安装在两片有机玻璃内的。当吉他以最大亮度显示白色时，功率消耗是 500 W，这本身就很了不起；没有哪个正常人会把吉他插到 500 瓦的功放里，即使是 100 瓦也太大声了。这里有更多的能量流向灯，而不是放大器，这太棒了。

简单地把发光二极管粘在吉他上并不会产生一个构建日志，那么这些像素是如何解决的呢？你如何用一束发光二极管制作显示器？这是一个严重的问题，但使用 Artnet 和 Resolume Arena 6，这些像素[可以映射到笛卡尔网格](https://learn.sparkfun.com/tutorials/using-artnet-dmx-and-the-esp32-to-drive-pixels?)，从那里它只是将视频放在吉他上。

虽然这个版本的第一部分很棒，并向您展示了电子产品在吉他中可以走多远，但这一部分是将一束 led 变成显示器的一个很好的演示，它不仅仅适用于一个巨大的 glowey 吉他。