# 如果有合适的老师，集成电路可以很容易理解

> 原文：<https://hackaday.com/2019/05/20/integrated-circuits-can-be-easy-to-understand-with-the-right-teachers/>

多年来，我一直试图理解硅芯片实际上是如何工作的。一块被故意污染的玻璃碎片是如何控制电子的？每隔一段时间，就会有人拿出一个学习辅助工具，让这些抽象的概念变得非常容易理解，在 Maker Faire Bay Area 的一个展位上就出现了这种情况。除了它给我的洞察力(和数以百计的 Faire-goers)，这里有一个关于 Maker Faire 所代表的最好的例子。你可以在下面找到他们演示的视频，以及展位上使用的道具的特写图像。

揭开硅的展台有一条横幅和一块桌布，但除此之外，它是如此的不起眼，以至于许多我与之交谈的人都忽略了它。[温德尔·奥斯凯](https://twitter.com/oskay)、[莲娜·埃德曼](https://twitter.com/1lenore)、[埃里克·施莱弗](https://twitter.com/tubetimeus)、[约翰·麦克马斯特](https://twitter.com/johndmcmaster)和[肯·希尔里夫](https://twitter.com/kenshirriff)拿出一块有 50 年历史的逻辑芯片，把它展示给任何想停下来问展出了什么的人。飞兆μL914 是一个双 NOR 门，它的年龄很重要，因为硅不仅简单，而且以今天的标准来看非常巨大，这使得个人黑客可以相对容易地使用工具窥视内部。

[![](img/395a99a4a0135235bea772b8a69b375c.png)](https://hackaday.com/wp-content/uploads/2019/05/maker-faire-ATmega328-decapped.jpg)

ATmega328 decapped by John McMaster was also on display at this booth

第一个挑战是到达骰子本身。这是约翰·麦克马斯特的专长，你可能从他的 [Silicon Pr0n](http://www.siliconpr0n.org/) 网站上熟悉这一点。他对芯片(以及运行 Arduino blink sketch 的 ATmega328)进行了解封，芯片暴露在外。参观者可以通过显微镜看到自己的电路。但看不等于懂，这也是这个展览的闪光点。

[![](img/7b44ea3313a479c04f6a4f9ec138bda0.png)](https://hackaday.com/2019/05/20/integrated-circuits-can-be-easy-to-understand-with-the-right-teachers/ul914-transistor-model-square/)[![](img/81aaa32ed2068c4d6f318b88b3996c56.png)](https://hackaday.com/2019/05/20/integrated-circuits-can-be-easy-to-understand-with-the-right-teachers/ul941-model-legend/)

为了让我们了解这个芯片是如何工作的，一叠激光切割的丙烯酸树脂展示了单个晶体管的基极、发射极和集电极。这个小模型的颜色编码和形状使得在芯片的完整模型上很容易挑出 941 的六个晶体管。这让你开始追踪电路的功能。

[![](img/235089d19b17995a5365662063085ee5.png)](https://hackaday.com/wp-content/uploads/2019/05/ul941-model-without-metal-layer.jpg) 对我来说，真正的啊哈时刻是设计中的电阻器。电阻层是通过在半导体中掺杂杂质，使其导电性更差而形成的。但是，如何对每个部分的期望电阻进行调零呢？这不是通过改变兴奋剂，保持不变。诀窍是让电阻本身占据更大的面积。更多的电子物理空间意味着更低的电阻，在这个模型中，你可以在右下角看到一个漂亮的胖电阻。这些模型的证明是展览的最后一件展品，因为硅芯片的艺术品是作为电路板布局的，带有用于重现原始芯片功能的分立晶体管。

在下面的视频中，Windell 带我们浏览了展台演示。我想你会对这些概念的分解以及它们对理解的帮助程度印象深刻。对于展览来说，这是一个绝妙的概念；它汇集了我所尊敬的跨学科专家，我关注他们的工作，并试图邀请每个人更好地了解隐藏在芯片中的秘密，这些秘密支撑着这个技术时代。这正是我喜欢在创客集会上看到的东西。

 [https://www.youtube.com/embed/VNzkhZBjo5k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VNzkhZBjo5k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

