# 罗兰 808 牛铃的工作原理

> 原文：<https://hackaday.com/2022/05/12/how-the-roland-808-cowbell-worked/>

每一代人都有一种乐器来定义自己的声音，对于那些在 20 世纪 80 年代形成音乐的人来说，Roland TR-808 打击乐合成器是一个非常有力的竞争者。它的声音可以从那个时代和此后每十年的大量热门歌曲中识别出来，尽管最初的乐器没有取得商业上的成功，但它仍然可以通过样本包、仿真和克隆获得。808 是一个不使用样本的全模拟设备，因此[Mark Longstaff-Tyrrell] [已经能够参考一些原始电路](http://www.frisnit.com/roland-tr-808-cowbell-rebuild/)再现其独特的牛铃声音。

当发现电路简单得令人耳目一新时，不应该感到太惊讶。触发脉冲被转换成控制一对振荡器的包络。混合输出经过带通滤波器，在输出端产生独特的声音，您可以在中断下方的视频中听到。该电路是在试验板上重建的，唯一的现代化让步是用一个微控制器代替原来的施密特触发振荡器。

总之，它提供了一个经典声音背后的合成迷人的洞察力，并让我们更加欣赏创造它的罗兰工程师的设计技能。我们之前已经看过 808 几次了，包括对导致其声音的著名故障晶体管[的解释。](https://hackaday.com/2018/09/06/you-cant-build-a-roland-tr-808-because-you-dont-have-faulty-transistors/)

 [https://www.youtube.com/embed/x-G5MUKNOy4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/x-G5MUKNOy4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



头图:布兰登丹尼尔衍生作品:Clusternote， [CC BY-SA 2.0](https://commons.wikimedia.org/wiki/File:Roland_TR-808_(large).jpg) 。