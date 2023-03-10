# 涨潮了，这个钟会告诉你

> 原文：<https://hackaday.com/2018/09/09/the-tide-is-high-and-this-clock-lets-you-know/>

如果你碰巧附近有海洋，你可能对涨潮和落潮很熟悉。如果泥滩徒步旅行是你所在地区的一件事，你也会意识到好的时机和知道水什么时候会回来的重要性。潮汐时钟将帮助你做好准备，它们是你平常时钟项目的有趣替代品。如果你正在寻找一个起点，[rabbitcreek]为教育目的组装了[一个基于 Arduino 的潮汐时钟套件。](https://www.instructables.com/id/Tiny-Moon-Tide-Clock/)

如果你觉得在这里有似曾相识的感觉，这确实不是[rabbitcreek]的第一个潮汐时钟项目。但与他之前的固定时钟不同，他现在创造了一个小巧便携的硬币电池版本，可以带着它出海。还有什么形状比 3D 打印的月亮更合适呢——不幸的是，目前的设计没有提供多少防水功能。

对于底层潮汐计算本身，[rabbitcreek]就像在他的上一个项目 [[Luke Miller]的基于位置的库](https://github.com/millerlp/Tide_calculator)一样，使用无处不在的 DS1307 和 DS3213 实时时钟。当然，如果你还想跟踪时钟上的其他事件，[为什么不为下一次涨潮](https://hackaday.com/2018/06/08/calclock-keeps-you-tied-to-the-mast/)设置日历事件呢？