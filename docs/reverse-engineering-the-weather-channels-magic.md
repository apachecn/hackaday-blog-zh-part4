# 逆向工程天气频道的魔力

> 原文：<https://hackaday.com/2021/03/14/reverse-engineering-the-weather-channels-magic/>

对于某个年龄段的美国读者来说，8s 上的 *Local 很可能在你心中占有特殊的位置。这个节目曾经是*气象频道*的主要节目，它将为观众提供文本，并最终以图形方式描述他们的当地天气预报，播放一些在电梯外听过的最棒的爵士乐。在智能手机甚至是常规互联网接入出现之前的日子里，从 20 世纪 80 年代到 21 世纪初，这些广播是规划你一天的重要组成部分。*

[![](img/aae66188a992ed55d95d0940ea16618d.png)](https://hackaday.com/wp-content/uploads/2021/03/ws4k_detail0.jpg) 直到最近，这些标志性天气报告背后的技术细节还鲜为人知，[但由于[techknight]](https://hackaday.io/project/178144-reverse-engineering-the-weather-star-4000) 的巨大努力，几十年来，WeatherSTAR 4000 机器抽取当前状况和*摇动全美各地有线电视分配中心的窝棚*的迷人工程现在被记录下来并保存下来。颠倒硬件和软件的过程实际上已经持续了几年，但所有这些有趣的细节现在终于可以在该项目的黑客日获得了。IO 页面。

这一切都始于 2018 年圣诞节前后，当时一个为 WeatherSTAR 4000 配置的易贝警报[techknight]终于发射了。他的提议被接受了，很快他就有了 8s 上 *Local 的物理表现在自己手中。他曾推断，让摩托罗拉 MC68010 机器工作就像在一台改装计算机中四处摸索一样，但没过多久，他就意识到自己已经进入了一个比他想象的要大得多的项目。*

问题是 WeatherSTAR 4000 被设计成将其所有软件作为提供实际天气数据的卫星下行链路的一部分。这台机器没有大容量存储器，所以所有的软件都储存在随机存储器里。一旦盒子被关掉，所有珍贵的代码就永远丢失了。

[![](img/5811bdf7d62296c150629beaf2713220.png)](https://hackaday.com/wp-content/uploads/2021/03/ws4k_detail.jpg) 尽管他尽了最大努力，[techknight]还是无法找到任何人能够捕捉到进入其中一个盒子的数据流，并且由于这一代硬件自 2014 年以来就没有使用过，[他似乎无法拿出一个 SDR 并自己记录下来](https://hackaday.com/2020/08/20/eavesdropping-on-satellites-for-fun-and-profit/)。长话短说:他独自一人。

接下来是我们见过的最令人印象深刻的逆向工程。花了几个月的艰苦劳动才完成电路板并创建新的原理图，之后他仍然不得不在没有一点原始文档的情况下处理 PALs 和散布在机器各处的早期 FPGAs。

在撰写本文时，[techknight]仍然在项目页面上以每天一到两篇新文章的形式记录逆向工程过程的最早期阶段。他要涵盖所有内容还需要一段时间，尤其是考虑到他在每篇文章中的深度，但我们当然不会抱怨。如果你想看看他目前的进程，[他总是在社交媒体上炫耀复活的 WeatherSTAR】。](https://twitter.com/techknight2)

如果你只是想重温那些 8s 上的本地记忆，自然[你会更喜欢树莓派和一点 Python](https://hackaday.com/2020/02/21/relive-the-glory-days-of-cable-tv-with-this-retro-weather-feed/) 。但是，对于拥有原始硬件来说还是有一些东西要说的，因为他现在拥有这个星球上可能唯一可操作的 WeatherSTAR 4000，我们相信[techknight]不会后悔他投入这个不可思议的项目的时间。

 [https://www.youtube.com/embed/3y4Yti3FxWg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3y4Yti3FxWg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 trhodes 的提示。]