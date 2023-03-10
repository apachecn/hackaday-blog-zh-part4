# 树莓派倒数到最后一个比特币

> 原文：<https://hackaday.com/2019/01/31/raspberry-pi-counts-down-to-the-last-bitcoin/>

尽管它可能看起来像是假装的互联网货币，但从设计上来说，比特币的数量是有限的。就像地球上有限的黄金数量和从地下开采黄金所需的努力使价格居高不下一样，比特币的稀缺性旨在确保其保持价值。截至目前，超过 80%的比特币已经进入流通领域。这听起来很多，但预计还需要 100 多年来释放剩余的，所以我们还有很长的路要走。

[![](img/a6a063efe00312db32b4e4d5fd23ca8e.png)](https://hackaday.com/wp-content/uploads/2019/01/btcticker_detail.jpg) 尽管当最后一枚比特币落入池中时，他的设备可能已经不存在了，[【Jonty】已经建立了一个股票，当最后一枚比特币从数字地下被开采出来时，它会倒计时](https://hackaday.io/project/163647-the-ultimate-bitcoin-tracker)。倒计时功能当然有点半开玩笑，但这个小工具也显示了稍微更相关的信息，例如比特币的当前价值，所以你可以永远记住，在它们还值几分钱的时候不投资是一个多么大的错误。

在硬件方面，这是一个非常简单的项目。该外壳是激光切割的 5 mm MDF，它包含一个 Raspberry Pi 3、一个 MAX7219 32×8 LED 点阵显示器和一个 10 mm 白色 LED 以及随附的电阻。白色 LED 放在丙烯酸漫射器后面，当设备通电时，显示器侧面的比特币标志会发出柔和悦目的光芒。滚动条上没有按钮或其他控件，一旦软件被配置好，只要插上电源就可以运行了。

至于软件，它采用了[Jonty]创建的 Python 脚本的形式，使用请求和漂亮的汤从[bitcoinblockhalf.com](http://www.bitcoinblockhalf.com/)收集相关数据。该脚本支持提取网站上列出的 19 个变量中的任何一个，并将其显示在 LED 矩阵上，这些变量从每日块生成等真正乏味的统计数据到任何数字钱包中有一些比特币的人可能希望在办公桌上滴答作响的合法有用的数据点。

[比特币的第一个十年是一段相当狂野的旅程](https://hackaday.com/2019/01/29/now-thats-what-i-call-crypto-10-years-of-the-best-of-bitcoin/)，不仅在货币方面，而且在如今参与加密货币开采和交易的各种硬件方面。[从比特币红绿灯](https://hackaday.com/2018/11/22/this-bitcoin-price-tracking-traffic-light-isnt-just-a-red-led/)到[定制的采矿钻机，如今它们更像是空间加热器](https://hackaday.com/2018/02/10/reverse-engineering-a-bitcoin-miner/)，支持这些虚拟货币需要大量的硬件。

 [https://www.youtube.com/embed/tMMky09HyKA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tMMky09HyKA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

