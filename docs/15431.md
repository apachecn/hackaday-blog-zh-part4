# 逆向工程“你不能在电视上说的七个单词(以及更多)

> 原文：<https://hackaday.com/2022/11/21/reverse-engineering-the-seven-words-and-more-you-cant-say-on-tv/>

尽管乔治·卡林很有远见，但他那句经典的“你不能在电视上说的七个字”大大低估了形势。至少从[【Ben Eater】对“TVGuardian 污言秽语过滤器”装置](https://www.youtube.com/watch?v=a6EWIh2D1NQ)的逆向工程来看，似乎实际数量至少是那个的 20 倍。

让我们从头开始，几周前[Alec]在每个人都喜欢的书呆子聚会技术连接上做了一个关于 TV guardian 的视频，这是一个试图清理直播电视和录制节目语言的设备。去看看那段视频的细节，但对于一个简短的总结，TVGuardian 的工作是扫描隐藏字幕文本，寻找不良词汇和短语，当在查找表中发现一些暗示性的内容时，将音频静音，并插入隐藏字幕替代攻击性内容。在他的视频中，[亚历克]渴望找到一种方法来查看禁止使用的单词列表，[本]接受了挑战。

淘气单词表最终保存在一个 93LC86 串行 EEPROM 上，本从他的 TVGuardian 中删除了它，以便进一步探索。他决定用 Arduino 滚动自己的解码器，而不是仅仅把它插入一个编程器，然后扔掉里面的内容，因为这样更有趣。我们能不能指出我们对[Ben]能够让观看别人的代码变得有趣的持续的惊讶？

当然，由此产生的 NSFW 单词表是令人兴奋的，如果视频就此结束的话，那将会非常令人满意。但是[Ben]走得更远，发现了列表是如何组织的，如何进行脏到干净的替换，甚至某些单词是如何被列入白名单的。最后一点导致了好莱坞传奇人物[迪克·范·戴克]得到了一个特殊的白名单，以免他的名字被净化成一个滑稽的[混蛋范盖伊]。

向[Alec]致敬，他激发了[Ben]令人着迷的逆向工程工作。

 [https://www.youtube.com/embed/a6EWIh2D1NQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/a6EWIh2D1NQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

