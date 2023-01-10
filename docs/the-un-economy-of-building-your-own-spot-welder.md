# 建造自己的点焊机不经济

> 原文：<https://hackaday.com/2018/09/21/the-un-economy-of-building-your-own-spot-welder/>

如果有一件事能让黑客们聚在一起，那就是用比购买更少的钱来建造东西的能力。这是一个测试[伟大的斯科特小工具]的练习，因为他正在摆弄一些 18650 锂电池，并且非常需要给电池贴上标签。这可以通过焊接来完成，但要正确完成，你真的应该使用点焊机。问题就在这里:你可以花 250 美元左右买一台点焊机，也可以花更少的钱造一台。[那么，问题来了:【大斯科特】应该造还是买点焊机](https://www.youtube.com/watch?v=5TVNdMqVZpk)？如果他是从易贝订单开始的，这就不值得一读了。

[Great Scott]围绕六个超级电容设计了这款点焊机，所有电容都用 Kapton 胶带牢牢固定在一起。这通过一组 MOSFETs，一切都通过一个 Arduino，一个旋转编码器和一个非常便宜的有机发光二极管显示器控制。这是一个足够简单的电路，但对于 perfboard 来说有点太过了，所以[Great Scott]设计了一个 PCB，并以不到 40 美元的价格获得了几块电路板。一点焊料和一些调试之后，*理论上*一个点焊机就造出来了。

做了那么多工作，点焊机是怎么工作的？但事实并非如此。原理图中的一个小失误意味着该板没有 MOSFETs 的参考地，因此所有这些工作都是徒劳的。当然，修理这块板唯一需要的是第二次旋转板，因为[伟大的斯科特]可能买了多余的零件*，因为这是聪明人做的事情*。尽管如此，他还是决定减少损失，搁置这个项目。

 [https://www.youtube.com/embed/5TVNdMqVZpk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5TVNdMqVZpk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[BaldPower]发送此邮件。