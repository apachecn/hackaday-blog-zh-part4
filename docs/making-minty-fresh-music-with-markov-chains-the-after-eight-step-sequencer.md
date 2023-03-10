# 用马尔可夫链制作清新的音乐:八步音序器之后

> 原文：<https://hackaday.com/2021/05/18/making-minty-fresh-music-with-markov-chains-the-after-eight-step-sequencer/>

步进音序器是很棒的乐器，但是它们可能有点重复。在它的核心，步音序器是一个非常简单的设备:它通过一系列音符或短语循环，这些音符或短语按顺序排列成各个步。操作者可以在音序器循环时改变步骤，但通常会有重复的感觉，因为音乐家不太可能抹掉所有步骤并在乐句之间输入全新的一组。

进入我们的老朋友机器学习。如果我们在循环的每一步引入一定的可变性，乐器可以在这里帮助音乐家，使最终的产品更有趣。当[Charis Cat]在八步音序器之后创造了[时，这样的乐器正是她着手制造的。](https://chariscat.wordpress.com/2021/02/14/generating-music-with-ai-combining-markov-chains-with-an-8-step-midi-sequencer/)

After Eight 是一个八步音序器，允许艺术家用一系列电位计设定每个音符(当然，电位计位于 After Eight 薄荷罐中)。电位计由 Arduino 读取，Arduino 将 MIDI 信息传递给运行流行的面向音乐的可视化编程语言 Max MSP 的计算机。该软件使用一系列马尔可夫链来增加音乐家输入的一系列音符，有效地与艺术家一起创作音乐。结果是一首美妙的音乐，每次演奏都不一样。请务必在最后查看视频，了解该项目的精彩概述(当然，也要听听 After Eight in action)！

[Charis Cat]的奇妙创造让我们想起了[Sara Adkins]所做的一些工作，[将人类的表现与复杂的算法](https://hackaday.com/2019/12/04/sara-adkins-is-jamming-out-with-machines/)融合在一起。这正是我们在 Hackaday 上喜欢看到的那种东西——音乐家的艺术意图与机器学习系统的随机不可预测性的融合，以产生独特的东西。

感谢[Chris]的提示！

 [https://www.youtube.com/embed/Zxq5JtLpzR0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Zxq5JtLpzR0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

