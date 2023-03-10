# CB 无线电+ Arduino = 6 米火腿乐队

> 原文：<https://hackaday.com/2019/08/05/cb-radio-arduino-6-meter-ham-band/>

不知何故[hvde]最终得到了一个在 11 米波段上做 AM 和 SSB 的 CB 无线电。问题是收音机在他住的地方是不合法的。所以他决定把收音机换成 6 米波段。

刚开始听到这个我们有点惊讶。大多数无线电电路被调谐到非常接近的容差，从 27 MHz 到 50 MHz 似乎是一个相当大的飞跃。答案？一个 Arduino 和一些其他精选电路。

特别是，[hvde]去掉了无线电的大部分射频部分，只留下处理 7.8 MHz 中频的部分。甚至发射机也产生这个频率，因为在固定频率下更容易产生 SSB 信号。Arduino 驱动频率合成器和有机发光二极管显示器。混频器将中频信号与 Arduino 命令的频率相结合。

收音机有一个“澄清器”,作为微调控制。有了新的设置，Arduino 也必须读取这个，并对频率进行小的调整。无线电中的射频电路也做了一些修改。这都是有记录的，尽管我们承认这可能不是一个心脏衰弱的项目。

尽管我们很欣赏这个项目，但我们认为我们会继续使用 SDR。如果你想了解更多关于[信号的数字合成](https://hackaday.com/2014/11/24/direct-digital-synthesis-dds-explained-by-bil-herd/)，查看【比尔·赫德】的帖子。

 [https://www.youtube.com/embed/XqOnwu77JaU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XqOnwu77JaU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

