# 为电动工具电池设计印刷适配器

> 原文：<https://hackaday.com/2020/03/30/designing-printed-adapters-for-power-tool-batteries/>

除非你特别喜欢多种类型的电池和充电器，否则你最好确保你所有的便携式电动工具都是由同一家公司制造的。但是，如果有一个工具你真的需要，但你选择的品牌不提供自己的版本呢？与其购买全新的工具生态系统，[你也许可以设计自己的电池适配器](https://www.thingiverse.com/thing:4239972)。

[![](img/8be847cf9258714d0a2f199674157435.png)](https://hackaday.com/wp-content/uploads/2020/03/batteryadapter_detail.jpg)

Note the locking tab that’s been printed separately.

正如[Chris Chimienti]在休息后的视频中解释的那样，你要做的第一件事(除了确保电压匹配之外)是仔细测量电池和工具上的连接器。他的目标是适应密尔沃基 M12 电池牧田 CXT 工具，所以如果你碰巧有相同的硬件组合，你可以只使用他的 STLs。否则，你将会用一把卡尺和一个记事本度过一段美好的时光。

一旦接口被设计和打印出来，它们就被连接在一起，并被安装到中心支撑柱的相对两端。从理论上讲，在这一点上你已经完成了，但是正如[Chris]指出的，这不仅仅是连接正极和负极。许多工具在电池中使用热敏电阻用于热保护目的，当工具没有从传感器获得读数时，它可能会拒绝工作。

他解决这个问题的方法是用一个适当阻值的标准电阻来“加热”电池连接器上的热敏电阻引线。这将使工具旋转，但显然没有更多的热保护。对于大多数房主 DIY 项目来说，这可能不会造成问题，但如果你是一个真正将工具推向极限的专业人士，这个项目可能不适合你。

当然，这并不是我们第一次看到有人将不同品牌的电池用于他们的工具。一旦你开始建立一个工作室，这是一个很常见的问题，尽管你可以[通过建立你自己的工具](https://hackaday.com/2019/03/05/3d-print-your-own-electric-screwdriver/)来避免它。

 [https://www.youtube.com/embed/nd4fHFHj9AU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nd4fHFHj9AU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

