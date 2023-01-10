# 灭虫者计数并为它的受害者唱小夜曲

> 原文：<https://hackaday.com/2022/06/11/bug-zapper-counts-and-serenades-its-victims/>

没有多少生物像蚊子一样被普遍鄙视，无论是无害的蚊子，在最坏的情况下，会让你错过冬天，还是更严重的蚊子，会对你的健康构成真正的威胁。处理它们的一个令人满意的方法是用球拍状的高压金属网灭虫器把它们轰掉。[lmu34]看到了一些额外游戏化的巨大潜力，[决定为他的 zapper 装备一个杀戮计数器和匹配的音效](https://www.instructables.com/Ultimate-Mosquito-Swatter-Mod-for-Gamer-Add-Kill-C/)。

最初的想法是，必须有一种方法来检测蚊子何时击中网格，并使用它来触发进一步的事件——在[lmu34]的情况下，播放一个声音文件并增加一个计数器。在拆开 zapper 并做了一些研究后，他将理论付诸实践，使用 Digispark Pro 板，其中包含 ATtiny167，用于播放一组 WAV 文件的 DFPlayer 模块，以及一个雄心勃勃的 4 位 7 段显示器来跟踪“分数”。一个新的 3d 打印盖子提供了足够的空间来容纳所有的组件，包括一个充电电路，因为他用一个可充电电池替换了原来的两个 AAA 电池，从而为显示器提供了更多的电力。

当然，在这些工作电压下，很难多次检测高压侧的活动，因此[lmu34]改用电流检测。他在这里区分了两个不同的等级，并将它们分别映射为大爆炸的*普通杀戮*和*怪物杀戮*，为每一个等级播放不同的声音。休息之后，请观看视频进行快速演示。

总而言之，这是一个令人愉快的荒谬的修改，几乎是为了让 ESP32 能够在下一次迭代中启用多人模式。但是，如果用低技术含量的小玩意追蚊子对你来说不合适的话，[还有激光](https://hackaday.com/2021/03/08/laser-zap-that-mosquito/)和[老式酷刑](https://hackaday.com/2021/03/08/laser-zap-that-mosquito/)，尽管这些不能被重新利用[在冬季做一些硬件故障注射](https://hackaday.com/2021/03/15/injecting-bugs-with-an-electric-flyswatter/)。

 [https://www.youtube.com/embed/_ZuR5MYr-M4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_ZuR5MYr-M4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

