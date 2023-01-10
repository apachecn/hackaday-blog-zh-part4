# 用这款树莓派 E-Ink 日历整理一下

> 原文：<https://hackaday.com/2019/02/11/get-organized-with-this-raspberry-pi-e-ink-calendar/>

像许多黑客一样，我们热爱电子墨水。这些图像变换和重组的方式令人着迷，而且具有明显的未来感。就像《哈利·波特》中的一些东西，但是你可以在阿里巴巴上买到，而不是在对角巷的商店里。但是任何使用过这项技术的人都会告诉你，电子墨水屏幕的低刷新率限制了它的潜在应用。它非常适合阅读书籍，但除此之外，它很难在廉价液晶显示器的世界中找到自己的位置。

但是[李宗霖]最近完成了一个项目，表明电子墨水至少还有一个用途:个人日历。你可以一天只更新一次屏幕，这样刷新率就无关紧要了，其他时间都是静态的，所以你也可以享受关闭屏幕带来的节能。有了一个幕后的 Raspberry Pi 从互联网上获取数据，它可以在日历上填充一切内容，从你的个人日程安排到你最喜欢的播客何时结束。

在实践中，[宗林]实际上每小时都在更新显示屏，因为他在屏幕的左上方显示了当前的天气状况，但即使如此，这仍然是电子墨水显示屏独特属性的完美应用。显示器是 Waveshare 的 7.5 英寸 640×384 型号，零售价约为 50 美元，因此在显示器、树莓 Pi 和一些可以将它们都放进去的东西(这里是一个相框)之间，这是一个非常便宜的构建[与那里的一些大格式电子墨水显示器相比](http://hackaday.com/2018/02/14/tearing-down-a-1000-e-ink-display/)。

软件部分是用 Python 3 编写的，宗林已经记录了其他人如何轻松地插入他们自己的信息，这样它就可以从谷歌日历中获取时间表数据，从开放的天气地图中获取当地情况。麻省理工学院许可的源代码也组织得很好，并有很好的评论，所以如果你想创建一个更全面的电子墨水家庭信息显示，这可以作为一个很好的基础。

如果这对你的口味来说似乎有点太单调，你总是可以[组装一个电子墨水电影播放器](https://hackaday.com/2018/12/30/the-very-slow-movie-player-does-it-with-e-ink/)，一个[功能惊人的 Linux 终端](https://hackaday.com/2018/08/14/run-a-linux-terminal-on-cheap-e-ink-displays/)，或者一个[非常光滑的基于 ESP8266 的名字标签](https://hackaday.com/2018/08/08/programmable-badge-uses-e-ink-and-esp8266/)。如果你得到了 1000 美元的大部分，但不知道该怎么花，[你甚至可以得到一个电子墨水牌照](https://hackaday.com/2019/02/01/digital-license-plates-are-here-but-do-we-need-them/)。