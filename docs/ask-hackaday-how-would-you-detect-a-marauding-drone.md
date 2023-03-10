# 问问 Hackaday:你如何发现一架正在劫掠的无人机？

> 原文：<https://hackaday.com/2019/01/01/ask-hackaday-how-would-you-detect-a-marauding-drone/>

过去几天，新闻中出现了无人机报道，伦敦盖特威克机场因大量无人机报道而关闭了几天。警方仍然感到困惑，逮捕了一对被证明是无辜的夫妇，并最终承认无人机有可能根本不存在。调查中出现的一个问题是，没有办法在地面人员的视野之外探测到无人机，正如我们在本文中已经探讨的那样，目击者的报告并不总是可信的。

[![Not much use against a small and mostly plastic multirotor. Sixflashphoto [CC BY-SA 4.0]](img/9f47b7a50446c46bc3018595ac5fe483.png)](https://hackaday.com/wp-content/uploads/2018/12/788px-KCMH_Radar.jpg)

Not much use against a small and mostly plastic multirotor. Sixflashphoto [[CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:KCMH_Radar.jpg)]

## 雷达看不到他们

乍一看似乎很奇怪，21 世纪的机场缺乏发现上空无人机的能力，但给 Hackaday 在业内的朋友打几个电话就清楚地表明，在典型的机场上使用雷达系统极难发现无人机。一个被设计用来在很高的高度追踪巨大的金属客机的系统，并不适合于在低空从侧面观察微小的、大部分是塑料的机器。我们被告知最多会出现断断续续的踪迹，但对于大多数无人机来说，雷达屏幕上根本没有任何踪迹。

我们确信，国防雷达领域的一些大公司正在排队向全球各地的机场提供价值数百万美元的系统，由于盖特威克的故事而陷入恐慌，投入了大量资金，但黑客空间中关于此事的闲聊让我们提出了一个问题:检测机场上空飞行的无人机有多困难？快速的谷歌搜索发现了多种声称是无人机探测器的产品，但如果它们有任何好处，盖特威克机场等机场难道不会已经在使用它们吗？黑客读者总是以他们的独创性给我们留下深刻印象，那么你会怎么做呢？

## 你能听到你看不见的东西吗？

作为一个普通的抄写员，提出这个问题很容易，所以开始吧，我首先想到的是我会怎么做。我总是听到多旋翼飞机的声音，然后抬起头去看它，所以我会采取听多旋翼螺旋桨独特声音的方法。高转速无刷电机的听觉信号能在机场附近的轰鸣声中被检测出来吗？

我在想象一个 Rasberry Pi 板网络，每个板上都连接着一个麦克风，进行一些实时音频频谱分析，以发现无人机可能的频率特征。当然，作为一个有出版行业背景的硬件人员，这么说很容易，那么一个软件专家也会这么做吗？或者你会选择雷达方法，甚至是红外线方法？当多旋翼飞机的部件在飞行中变得非常热时，你能感觉到它的热信号吗？

无论你认为什么可以作为无人机探测系统，在评论中给它一个旋转。我们建议人们要有信心去建造一些东西，甚至可能在时机成熟时参加黑客日奖。来吧，你有什么损失！