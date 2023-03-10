# 由于监管原因，开源无源雷达被关闭

> 原文：<https://hackaday.com/2022/11/19/open-source-passive-radar-taken-down-for-regulatory-reasons/>

开源技术带来了一个法律法规还没有完全准备好的世界。因此，有时，开放项目需要绕过政府法规。在今天的新闻中， [KrakenRF 团队在他们基于 KrakenSDR 的被动雷达代码上遇到了武器交易的法律障碍](https://forum.krakenrf.com/t/where-has-the-passive-radar-code-gone/98/3)，目前正在解决这个问题。没有迹象表明美国政府采取了任何法律行动——车队很主动，[就像我们被告知的那样。](https://twitter.com/rtlsdrblog/status/1591657740229046274)

简化一下，KrakenSDR 硬件是一块 PCB 上的五个 RTL SDR——需要做大量的工作才能做到正确。它比几个加密狗让你走得更远——有屏蔽外壳、合适的连接器、可靠的配电、适当的 USB 集线器，以及重要的是，接收器同步硬件。自然，你可以用这样一个沉重的包建造一些好东西——其中之一是被动雷达，这是 2021 年 KrakenSDR 的[预发布页面、](https://web.archive.org/web/20210914080844/https://www.crowdsupply.com/krakenrf/krakensdr)和[一周前的众筹页面](https://web.archive.org/web/20221106002301/https://www.crowdsupply.com/krakenrf/krakensdr)上的一个突出卖点。这是怎么回事？

除非你在海上或沙漠中，否则你周围的空气中会飘着射频辐射。无论是飞机转发器、手机发射塔，还是蹩脚的开关模式 PSU，发出的无线电波都会与你周围的物体相互作用。如果您有多个带有定向天线的接收器，您可以捕捉从某个对象反射的波，将反射波与从初始源接收的波进行比较，并确定该对象的属性，如位置和速度。如果你想知道更多，IEEE Spectrum 已经在一周前[报道了这个话题](https://spectrum.ieee.org/passive-radar-with-sdr)，之前被删除的 [KrakenSDR wiki 页面](https://web.archive.org/web/20221004071929/https://github.com/krakenrf/krakensdr_docs/wiki/08.-Passive-Radar/)有更多的细节供你学习。

通过在 IEEE 频谱中的曝光，KrakenSDR 的工作得到了大量的关注和评论。这就是国际武器交易条例(ITAR)的由来。我们不是律师，但是[it*看起来像是被动雷达在名单上。*](https://www.ecfr.gov/current/title-22/chapter-I/subchapter-M/part-121)*如今，当团队与法律专家交谈时，代码库和文档页面被清理干净。*

 *处理这种情况是令人生畏的，我们希望他们能顺利通过法律途径解决这个问题。在过去糟糕的日子里，[某些加密算法在 scope](https://en.wikipedia.org/wiki/Export_of_cryptography_from_the_United_States) 中很出名，这在当时对我们来说是绝对荒谬的。法律最终确实发生了变化，以更好地反映现实，但正义的车轮转动缓慢。*