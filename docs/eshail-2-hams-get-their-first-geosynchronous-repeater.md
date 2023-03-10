# Es'hail-2: Hams 获得首个地球同步中继器

> 原文：<https://hackaday.com/2019/03/18/eshail-2-hams-get-their-first-geosynchronous-repeater/>

在广播行业，占据高地是用尽可能少的设备覆盖尽可能多的区域的关键。任何引人注目的东西，从大型市政水箱到路边广告牌，再到偏远的山顶，都可能布满天线，不同的服务公司争夺放置天线的最佳位置。业余无线电俱乐部也会在那里，寻找放置中继器的空间，这使得业余爱好者可以使用低功率移动和手持无线电在比其他方式大得多的范围内进行联系。

现在，一些火腿已经为他们的中继器占领了最高的高地:太空。第一次，一个业余无线电中继站搭乘地球同步卫星进入太空，使 hams 有能力连接超过三分之一的地球。这是一个巨大的发展，虽然使用这种新的天基无线电需要一些努力，但它是业余无线电界的游戏规则改变者。

## 高层的朋友

这颗名为 [*Es'hail-2*](https://en.wikipedia.org/wiki/Es%27hail_2) 的新卫星是为卡塔尔电信公司 Es'hailSat 建造的。就卫星而言，这是一个非常标准的机器，主要用于向中东和非洲提供直接的数字电视服务。但有趣的是，它从一开始就被设计成携带业余无线电有效载荷。Es'hailSat 在 2014 年初向潜在供应商发出的[征求建议书](https://www.broadbandtvnews.com/2014/03/21/eshailsat-issues-rfp-for-eshail-2/) (RFP)特别呼吁加入一个业余转发器，由业余无线电卫星公司 AMSAT 联合开发。

[![](img/01f720d79031ac32042bfb53b5802d28.png)](https://hackaday.com/wp-content/uploads/2019/03/expert-01.png)

The other kind of networking. His Excellency Al-Attiyah (A71AU). Source: [Al-Attiyah International Foundation for Energy and Sustainable Development](https://www.abhafoundation.org/)

Es'hail-2 上的中继器是由卡塔尔业余无线电协会(QARS)、Es'HailSat 和德国 AMSAT 集团的 AMSAT-DL 联合开发的。Es'HailSat 公司愿意在一架商用飞机上安装业余无线电有效载荷的部分原因可能是，QARS 公司的主席是卡塔尔前副首相 Abdullah bin Hamad Al Attiyah 阁下(A71AU)。

中继器的设计考虑了两个主要服务。第一种是窄带转发器，用于电话(语音)联系，连续波(CW)用于莫尔斯联系，以及一些窄带数字模式，如 PSK-31。另一个转发器用于宽带用途，旨在测试数字业余电视(DATV)。宽带转发器可以同时传送两个高清信号和一个广播 QARS 视频内容的信标。两个转发器都在为 hams 保留的 2.4 GHz 部分上行，而在 10.4 GHz 频带下行。

2018 年 11 月 15 日，Es'hail-2 搭载 SpaceX 猎鹰 9 号从卡纳维拉尔角发射升空。这颗卫星被推进位于东经 26.5 的拥挤的轨道中的地球同步轨道，停在刚果民主共和国的正上方。测试完成后，2019 年 2 月 14 日举行了卫星命名为“卡塔尔奥斯卡-100”，或 QO-100 的仪式，这是第 100 颗由业余爱好者发射的[奥斯卡卫星](http://hackaday.com/2016/01/14/hams-in-space-project-oscar/)。

## 监听

遗憾的是，对于美洲和东亚大部分地区的火腿来说，QO-100 超出了范围。但是对于从巴西沿海到泰国的任何地方的火腿来说，卫星一天 24 小时都是可见的。如果挪威这个业余无线电俱乐部的经历可以作为参考的话，那么使用它的设备可能会令人生畏。他们使用了一个 3 米的碟形天线进行 2.4 GHz 的上行链路，以及一系列自制硬件和很大的决心来完成他们迄今为止的一次接触，这来自一个用来从月球上反弹信号的团队。

从 QO-100 接收信号要容易得多。一个 60 厘米至 1 米范围的碟形天线就足够了，取决于位置，配有一个不错的 LNB 下变频器。几乎任何 SDR 都可以作为接收器。除了自己组装硬件之外——这也是卫星覆盖不到的地球上三分之二地区享受乐趣的唯一方式——可以收听已经建立的 WebSDR 地面站。英国业余电视俱乐部和位于 Goonhilly 地球站的 AMSAT-UK 已经为窄带转发器设置了一个 SDR，你可以通过网络控制它。那天晚上我用它监听了哈姆之间的一些联系。

 [https://www.youtube.com/embed/NgsnyETnjAs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NgsnyETnjAs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



很难夸大 QO-100 的重要性。这是地球同步轨道上的第一个业余无线电转发器，也是太空中的第一个 DATV 转发器。这是一个相当大的成就，它将允许火腿在工作中发展的技能这只鸟将为下一代火腿卫星的设计提供信息。向所有参与 QO-100 飞行的人致敬！