# 小小的 MIDI 钢琴用螺线管唱歌

> 原文：<https://hackaday.com/2019/08/13/itty-bitty-midi-piano-sings-with-solenoids/>

玩具钢琴弹一会儿很有趣，但是它们的小键盘和更小的声音很快就让它们在音乐上变得索然无味。[曼斯·乔纳松]找到了一种让一架两个八度的玩具钢琴变得几乎面目全非的方法。它只需要三十个螺线管，几个 Arduinos，一个 MIDI 盾，以及大量的时间和耐心。

这架钢琴的琴键利用杠杆作用敲击薄钢叉。这些尖齿的间隔宽度刚好能让小小的 5V 螺线管套在上面。一旦[MnS]通过 MIDI 输入获得了一个螺线管，他就开始设计 3D 打印支架，将它们固定在共鸣板上。

所有 30 个螺线管就位后，一切都运转正常，但在他升级到马达驱动护盾之前，线路是一团乱麻。然后，他设计了一个新的支架，可以同时容纳八个螺线管，每对电线都有一个通道。每八个螺线管，就有一个 Arduino 和一个电机屏蔽。

由此产生的初级演奏者钢琴听起来就像有人在演奏木琴之类的风铃，或者加勒比海的小钢鼓。休息之后，请观看构建视频。

讨厌玩具钢琴的声音，但喜欢方便的外形？[把一个变成合成器](https://hackaday.com/2016/05/20/toy-piano-gets-synth-overhaul/)。

 [https://www.youtube.com/embed/Avnidj0R3Yg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Avnidj0R3Yg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

