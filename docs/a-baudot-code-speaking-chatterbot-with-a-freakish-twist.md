# 一个说博多语的奇怪的聊天机器人

> 原文：<https://hackaday.com/2022/04/26/a-baudot-code-speaking-chatterbot-with-a-freakish-twist/>

[Sam Battle]在 YouTube 上被称为[Look Mum No Computer],通常被认为是一名音乐艺术家，但最近似乎对复古的电信设备有点兴趣，这一最新的尝试是进入 minicom tty 设备的领域，这是那些听力不够好的人通过电话交流的生命线。由于在这个通过互联网聊天的现代时代，找到另一个拥有迷你通讯器的用户变得越来越困难，[Sam]决定[将人类完全排除在外，让迷你通讯器用户与运行 MegaHal](https://www.youtube.com/watch?v=OYJti8dJMV4)实例的 Raspberry Pi 交谈，这是 20 世纪 90 年代的聊天机器人。这个建筑的想法(成为这个博物馆的一个展品并没有过时)是在房间周围有许多 minicom 终端通过内部电话网络(和复古电话交换机{ Sam }维护)连接到一个线路接口模块，基于 [Mitel MH88422](https://www.semiee.com/file/EOL/Mitel%20-MH88422.pdf) 芯片。这个方便的设备允许 Raspberry Pi 连接到电话线，接听电话，并处理所有常见的握手。来自 Mitel 接口的音频信号通过 USB 音频接口(因为 Pi 没有音频输入)模块输入到 Pi。

minicom 说出 [Baudot code](https://en.wikipedia.org/wiki/Baudot_code) ，将输入的字符编码成另一端可以解码的音频流，因此这也需要由 Pi 来处理。由于法典本身可以追溯到 19 世纪 70 年代，这可能不是![](img/36d7e2cf284b7a6a85e8e3cd920d00ac.png)实施的一件大事。 [MegaHal](https://en.wikipedia.org/wiki/MegaHAL) 使用了一个基于[隐马尔可夫模型](https://en.wikipedia.org/wiki/Hidden_Markov_model)的模型，它可以被认为是人工智能系统的一个例子，这取决于你的观点。MegaHal 的模型可以生成(有时！)在适当的数据集上训练之后，来自一些输入文本的可理解的句子。[Sam]的合作者[MarCNeT]出于培训目的使用了[Sam]歌曲中的歌词。minicom 到 MegaHal 的接口完成后，这对于[Sam]来说还不够，所以他在他那有点恐怖的 Kosmo 作品中添加了一个额外的接口，在混合中添加了一些牙齿和眼球运动。一个 sparkfun 音频触发器给了 Kosmo 它的声音，尽管我们认为 Pi 可能也能做到这一点。如果你想了解设计过程，你可以[阅读文字记录](https://lookmumnocomputer.discourse.group/t/baudot-minicom-5000-stuffs/3895/9)，但这还不够，如果你离得够近，你可以去[这个博物馆(没有)过时](https://this-museum-is-not-obsolete.com/)，亲自去看看。

在这些地方，与人工智能相关的恶作剧并不少见。这里有一个有趣的 [clickbait 生成器](https://hackaday.com/2015/10/15/73-computer-scientists-created-a-neural-net-and-you-wont-believe-what-happened-next/)，然后有一种方法[让 Linux 做你想做的](https://hackaday.com/2021/04/20/ai-makes-linux-do-what-you-mean-not-what-you-say/)，而不一定是你所说的，最后，如果这对你来说太牵强，不够实用，你可以[黑掉你的咖啡机，在你最需要的时候学会为你蒸](https://hackaday.com/2021/09/09/ai-powered-coffee-maker-knows-a-bit-too-much-about-you/)。

 [https://www.youtube.com/embed/OYJti8dJMV4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OYJti8dJMV4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

