# 你不能修正你不能测量的东西

> 原文：<https://hackaday.com/2021/07/10/you-cant-fix-what-you-cant-measure/>

去年，作为我的 Corona 爱好，我开始驾驶遥控飞机。我从铁饼发射的滑翔机开始，老实说，这仍然是我的主要爱好，但在设计成绝对最小重量和最大性能的飞机上，只有这么多空间可供黑客攻击；这种飞机会注意到尾部多了半克。所以我也造了几架粗糙的重型飞机——那种你可以把一台 60 g 的十年前的 GoPro 放上去，它甚至不会真正注意到的东西。有些已经在树上结束了它们的生命，但是大多数已经被分解并转世——电子在下一个身体里继续存在。

旅程真的很有趣。我学习了空气动力学，找了一个借口组装了一个 4 轴热线数控聚苯乙烯泡沫切割机，并用碳纤维丝束覆盖了视线内的一切，这比你想象的要便宜，但使飞机进入了太空时代。我目前的老爷车已经安装了 IMU、GPS 和一个最小的 Ardupilot 设置，尽管我还没有真正测试过它。阻碍我的是视频链接——它在几百米以外就无法可靠地工作，我当然不相信它会离开视线。

我怀疑是我那些蹩脚的天线拖了我的后腿，这当然是对 DIY 的鼓励，但在 5.8 GHz 频段测量天线是很棘手的。我很想能够买一个我们在过去[报道过的](https://hackaday.com/2019/08/11/nanovna-is-a-50-vector-network-analyzer/)[廉价矢量分析仪](https://hackaday.com/2018/03/29/putting-a-poor-mans-vector-analyzer-through-its-paces/)——任何人都可以在看到自己在做什么时制作天线——但它们的最高频率为 2.4 GHz 或更低。没有骰子。5.8 GHz 我就瞎了。

当然，我确实有一种方法，那就是接入专用 5.8 GHz 接收机的接收信号强度指标(RSSI)，并在实践中测试天线，但这只能给出一种松散的更好-更差的指示。电容多还是电感多？板块靠得更近还是离得更远？试试看，我猜，但是很费时间。

这个故事的寓意:不要认为测量设备是理所当然的。想象一下，尝试在没有电压表的情况下构建模拟电路，或者在没有逻辑探针的情况下调试数字电路。有时候最重要的工具是让你首先发现问题的工具。

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!