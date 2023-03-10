# 扩展板将 Spotify 放在 Amiga 500 上

> 原文：<https://hackaday.com/2020/03/20/expansion-board-puts-spotify-on-the-amiga-500/>

毫无疑问，观众中的一些纯粹主义者会称这是作弊，因为这部 1987 年的 Amiga 500 在技术上并没有连接到 Spotify 并自己播放音乐。但我们也怀疑这些人可能忽略了一个名为 Hackaday 的网站。有了[【丹尼尔·阿维德森】千方百计促成此事](http://crowstudio.se/how-to-play-spotify-on-your-a500/)，如果不是黑客还能是什么？

这个项目，就像现在很多项目一样，从树莓派开始。不要担心 Amiga 爱好者，这台经典的机器没有被掏空，它的内部被一个小巧的 Linux 板取代。但是多亏了被称为 A314 的扩展卡，你可以说它接受了企鹅注入。这种智能板允许内部安装的 Raspberry Pi 通过共享内存与 Amiga 500 通信，从而使各种欺骗成为可能。

在这种情况下，Raspberry Pi 实际上是用`raspotify`连接到 Spotify Connect 服务并解码流的那个。但是由于一些管道和一个 ALSA 插件，音频本身实际上被推入了 Amiga 的声音硬件。在休息后的视频中，这个过程用适合这种老式计算机的曲调进行了演示。

这一过程类似于一个经典的苹果粉丝如何让 Spotify 在他们的 Macintosh SE/30 上运行，对老式硬件也有类似的尊重。当然，如果你真的*想要*把你的 Amiga 500 掏空，换成树莓派，我们[已经看到了一些非常好的转换，让你开始](https://hackaday.com/2018/03/25/an-amiga-500-for-the-21st-century/)。

 [https://www.youtube.com/embed/i_iyzuP45rc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/i_iyzuP45rc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 burningbroccoli 的提示。]