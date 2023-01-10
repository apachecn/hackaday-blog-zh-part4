# Sonos 和亚马逊智能扬声器的拆卸揭示了有趣的工程细节

> 原文：<https://hackaday.com/2018/07/12/teardown-of-sonos-and-amazon-smart-speakers-reveals-interesting-engineering-details/>

拆开东西总是很有趣，这个[打开 Sonos One 告诉我们关于 Sonos IPO 的事情>【Ben Einstein】对 Sonos 和亚马逊智能扬声器的拆卸的精彩报道](https://techcrunch.com/2018/07/09/digging-deeper-into-smart-speakers-reveals-two-clear-paths/)展示了你可以学到的东西。[Ben]是一名风险投资家和工程师，所以他的大部分文章都集中在这些设备说明了公司如何花钱。不过，黑客还有很多东西要学:他详细介绍了 Sonos One 如何使用 PCI 子板进行无线通信，而亚马逊 Echo 的主板上有一个可编程无线电。

Sonos 方法的优点是您可以在多个型号上使用同一个子板:只要每个型号都有 PCI Express 插槽，您就可以将子板插入其中任何一个。亚马逊的方法更贵，但有一个巨大的优势:无线电可以重新编程，远程支持其他无线标准。[Ben]指出，这表明两家公司有着不同的方法:Sonos 试图通过制造可以在不同型号上使用的模块来节省资金，而亚马逊在设计和组件上花了更多的钱来创造一种可以处理当前和新标准的设备。

> 这是另一个线索，亚马逊正在考虑将 Echo 作为一个家庭网关，而不是一个有一些新技巧的扬声器…如果不认真研究每个定制零件和购买的组件，估计 BOM 成本总是很棘手，但我怀疑，尽管价格标签低 25%，但 Echo Plus 比更高端的 Sonos One 贵 15-20%。

[Ben]并不认为 Sonos 在与亚马逊的长期竞争中会做得很好。我对这个市场了解不多，无法判断他在这方面的论点，但很值得阅读他的文章，看看两家制造商都使用的整洁的工程技巧和选择。另外，看到一个个小玩意总是很有趣。

[通过 Techcrunch]