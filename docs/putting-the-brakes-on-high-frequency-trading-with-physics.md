# 用物理学给高频交易踩刹车

> 原文：<https://hackaday.com/2019/02/26/putting-the-brakes-on-high-frequency-trading-with-physics/>

在 2018 年夏天东海岸的缓慢炙烤中，一个奇怪的现象浮出水面。随着热带气团在纽约大都市地区定居并窒息，随着连接各种数据中心和交易所的微波信号开始变慢，某种类型的股票投机者开始感受到金融热。这些高频交易者依靠在其他交易者看到同样的事情之前几分之一秒获得信息，并利用微小的价格差异赚钱。

虽然你不会看到我们为这些投机者在炎热天气期间损失的数十亿美元流泪，但我们确实发现了这样一个事实，即湿度可以减缓微波传播，足以使这个问题成为他们的一个迷人主题，以至于我们当时报道了一些细节。虽然金融市场来来去去，利用金融市场的技术日新月异，但物理学却保持不变，它可以在不考虑所谓基本面的情况下达成或破坏交易。

因此，我们怀着极大的兴趣看到了汤姆·斯科特最近的一段视频，该视频描述了一家新的证券交易所如何利用物理技术来减缓股票交易的速度，试图获得相对于其他交易所的竞争优势。鉴于今年夏天传播延迟仅 10 微秒就造成了数十亿美元的损失，我们不禁想知道，使用“神奇鞋盒”注入 35 倍的延迟实际上对业务有什么好处。这是一个有趣的故事。

 [https://www.youtube.com/embed/d8BcCLLX4N4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/d8BcCLLX4N4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 公平竞争

简单回顾一下，高频交易(HFT)试图从数百万笔计算机执行的高速交易中赚取一小部分利润。HFT 公司一次赚很多钱，通过购买并持有股票仅几分之一秒，然后以略高的价格将其出售给其他人来获利——或者，通过以高价借入股票并在几毫秒后以较低的价格出售股票来“做空”股票，一旦股票回归，就通过差价获利。“低买高卖”这一古老的建议已经推动了金融市场几个世纪，只是随着 HFT 服务器系统在每个主要证券交易所的数据中心内的同处一地以及上述微波链路以低延迟访问最新信息，这一建议得到了大力推动。

但 HFT 公司还有另一种方法将微秒转化为微利:潜伏套利。基本上，它包括使用 HFT 系统挑选出所谓的“陈旧报价”，这是由于不同市场经常需要几毫秒来更新价格。一个 HFT 程序在一个交易所寻找陈旧的报价，然后迅速向另一个具有不同陈旧信息的市场发送买卖该股票的指令，利用价格差异。有时 HFT 项目会胜出，给 HFT 公司带来微薄的利润。一天做几百万次，你就有了一个商业模式。

## 神奇的鞋盒

这种商业模式最终对市场造成了很大损害，由于 HFT 算法扑向陈旧的报价，往往会人为推高一些股票的价格。为了平衡局面，新贵 IEX 证券交易所决定尝试一些激烈的举措。他们推断，通过减缓所有通过他们交易所的交易，他们可以防止潜伏套利。

[![](img/8c53ef5df066ae48b740c24e34947c24.png)](https://hackaday.com/wp-content/uploads/2019/02/magic-shoe-box.png)

The “Magic Shoebox” – 61 km of fiber optic cable introduces a 350-microsecond delay to all trades. Source: [IEX](https://iextrading.com/)

为此，他们在 IEX 新泽西州威霍肯的数据中心安装了“神奇鞋盒”，这是一个带有三个线轴光纤线路的机架安装式机柜。这三个卷轴，每个的大小都和 3D 打印细丝卷轴差不多，连接在一起形成一个 61 公里(38 英里)长的连续环。这个长度是经过计算的，为进出交易所的所有流量引入了精确的 350 微秒延迟，包括连接交易所设施的 16 公里(10 英里)光纤电缆。一切都要经过延迟线，包括试图寻找过时报价的 HFT 系统。但这种延迟让来自多个市场的信息有时间通过系统过滤，消除了过时报价被剔除的可能性。

在一个越快越好的世界里，IEX 颠覆了传统智慧，找到了制胜策略。他们神奇的鞋盒不仅消除了潜在套利，还让 IEX 比其竞争对手更有优势，这些竞争对手已经按照他们的方式推动了业务。IEX 通过了美国证券交易委员会(SEC)漫长而艰难的申请过程，最近获得了正式股票交易所的地位，这让 HFT 公司和一些老牌交易员非常懊恼。

他们仍然在用他们的 350 微秒的减速带做生意，尽管用的是新版本的魔法鞋盒。尽管有人诋毁他们，但他们已经证明，他们可以在金融市场上公平竞争，以至于美国证券交易委员会(SEC)发布了一份白皮书，称赞新交易所对市场的整体积极影响。他们在简单物理学的帮助下完成了这一切。