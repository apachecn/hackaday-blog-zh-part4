# 在应用笔记的赞美中

> 原文：<https://hackaday.com/2019/04/02/in-praise-of-the-app-note/>

当我在电子世界里找不到解释的时候，我会去找我的大拇指*霍洛维茨&希尔*。当 *H & H* 让我失望的时候(这种情况并不常见)，我很可能会发现自己在看一家半导体公司的求职信，这家公司为了吸引我的注意力，正在与竞争对手展开激烈的竞争。这些公司有广泛的销售和营销努力，其中一部分来自知识的传播。

剃须刀片可能会卖给年轻人，上面有喷气式战斗机的图像和一个微妙的暗示，即一个剃光胡子的家伙得到了他的女孩，但半导体品牌是通过用信息激起工程师的兴趣来销售的。为了这个目的，公司变成了赞扬他们产品的出版社。他们不仅制作处理单个设备的数据表，还制作涵盖更广泛主题的应用笔记文档，并讲述为什么这家制造商的零件自然是世界上最好的。

这些应用笔记经常会成为引人入胜的读物，如果你还没有找到它们，你应该去半导体商业网站的文档部分寻找一些。

## 一个免费的参考图书馆(有一点产品植入)

[![A selection of probes, from [Jim Williams'] Linear Technology app note 72.](img/5a3d5287030dedd505b6def3094b459b.png)](https://hackaday.com/wp-content/uploads/2017/03/lt-probe-configurations.jpg) 

Jim Williams 选择的示波器探头包括他的手出现在不止一个 LT 应用笔记中，并启发了几年前我们的一篇愚人节文章。

数据手册信息丰富、内容全面，但本质上仅限于单个器件或几个近似相同的器件。应用笔记更类似于一篇关于更广泛的工程问题的技术文章，最好的应用笔记几乎可以被视为类似于我的 *Horowitz & Hill* 中的一个章节——一旦你阅读了它们，你就对它们所涵盖的主题有了彻底的了解。有时，他们可以在一个困难的项目上拯救你，正如我在一份对高压反激式转换器有严格要求的合同中所做的那样。

从 LT 应用笔记开始是合适的，因为它的作者是模拟工程大师和应用笔记的老前辈，已故的[吉姆·威廉姆斯](https://en.wikipedia.org/wiki/Jim_Williams_(analog_designer))。在从 20 世纪 70 年代末到 2011 年英年早逝的职业生涯中，他写了大量这样的作品，首先是为国家半导体公司，然后是为 LT 公司，这些作品既深刻又全面，同时包含机智、幽默，当然最后一页还有他标志性的手绘漫画。他下面的漫画来自 LT AN49 [*液晶显示器*](https://www.analog.com/media/en/technical-documentation/application-notes/an49.pdf) 照明电路。

![](img/fa629618284100f7803ca0f2123e62a3.png)

我从他的 LT 应用笔记中学到了很多，如果我能稍微模仿一下他的写作，我作为一名黑客作者的生活就完整了。还有谁能写出像 LT 的 AN25，标题为“ [*【诗人的开关调节器】*](https://www.analog.com/media/en/technical-documentation/application-notes/an25fa.pdf) ”或 AN47、 [*高速放大器技术*](https://www.analog.com/media/en/technical-documentation/application-notes/an47fa.pdf) 这样的东西，这是手头这个主题的开创性工作。我并没有全部读完，我应该在某个时候坐下来，努力纠正这个疏漏。

## 每个人都在做

当然，虽然这让我有机会对某个作者的作品大加赞赏，但所有主要的半导体公司都会制作应用笔记。有时它们只不过是数据手册信息的干巴巴的集合，但其中仍然有任何工程师都应该从中有所收获的作品。

![](img/fcb5322f0bac8c568ca8f5195be3492c.png) Maxim Integrated 的*为工作选择正确的调节器*系列以这种方式接近书籍长度，分为 3 部分，带有应用程序注释 [5998](https://www.maximintegrated.com/en/app-notes/index.mvp/id/5998) 、 [5999](https://www.maximintegrated.com/en/app-notes/index.mvp/id/5999) 和 [6071](https://www.maximintegrated.com/en/app-notes/index.mvp/id/6071) 。我发现另一个很有帮助的此类文档是 t I 的 [AN058 *天线选择指南*](http://www.ti.com/lit/an/swra161b/swra161b.pdf) ，它为读者提供了常用 ISM 频段所有类型 PCB 天线的全面入门。有一种观点认为，对于工程师来说，设计自己的 PCB 天线是一个黑洞，但如果你想这样做，这篇应用笔记将证明是一个无价的资源。

应用笔记的一个典型功能是查看参考产品设计，其详细程度远远超过所用器件的数据手册。恩智浦的[an 11401*tea 1720/tea 1705 5 W 至 12.5 W 电源/USB 充电器*](https://www.nxp.com/docs/en/application-note/AN11401.pdf) 中显示的电源就是这种类型的典型例子，在恩智浦工程师的辛勤工作下，公司希望像这样的设计能够完全融入客户产品。这些参考设计应用笔记并不总是以集成电路为特色，例如，带滤波器的 2SK3557/D [*AM 无线电放大器模块使用 2SK3557*](https://www.onsemi.com/pub/Collateral/AND2SK3557-D.PDF) 是一个以 FET 为特色的 ON Semi 文档。

![](img/982adddb8be0648de31ca7703cb185ca.png)

Basic Application Schematic from the NXP AN11401 app note on USB charging

大多数读者可以花一个愉快的下午、一天甚至一周的时间浏览半导体应用笔记，因为其中有如此丰富的有趣内容有待发现。但是我们只有一篇 Hackaday 文章的空间来列出它们，所以如果你们中的任何人有最喜欢的应用笔记，请在下面的评论中添加它们。如果应用程序笔记的世界对你来说是新的，那么你就可以享受一下了！潜入离你最近的半导体公司的网站，开始阅读吧！