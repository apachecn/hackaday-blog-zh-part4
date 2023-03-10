# 自定义压缩将经典的计算机合唱压缩到一个微型控制器中

> 原文：<https://hackaday.com/2021/08/19/custom-compression-squeezes-classic-computer-choruses-into-a-tiny-controller/>

某个时代的极客们会对以今天的标准来看过于简单的游戏有着美好的回忆，但还是画了一个。他们的低保真度图形经常被同样低保真度的音乐所补充，这些音乐是通过大多数计算机中的扬声器的事后想法而被迫播放的。尽管有那个时代的技术限制，这些游戏不仅仅提供游戏性。他们讲故事，他们身临其境，有些人会认为这与年轻一代无关。

这并没有阻止[Thanassis Tsiodras]在他的侄女和侄子小时候分享经典的《猴岛的秘密》。在因新冠肺炎事件而分离一年后，见到家人很兴奋，[Thanassis]想给他们一份手工制作的礼物:[用定制播放器播放《猴岛的秘密》中的音乐](https://www.thanassis.space/monkeyisland.html)。多好的大叔啊！

[Thanassis]本可以使用任何数量的芯片录制音乐并播放，但作为一名长期的软件工程师，他决定走风景优美的路线到达目的地。首先，DOSBox 被黑客攻击，将扬声器输出转储到一个文件中。Python、C 语言和 30 年的经验被用来将所有东西都压缩到 ATtiny85 的 8 KB 存储中。这样做并不容易，因为这需要他创建一个自定义的霍夫曼压缩实现，以使数据足够小，适合芯片。当它适合，但不工作，甚至更多的优化是必要的。

然而，最终的结果是值得的，来自“猴岛的秘密”的音乐以其原始形式从一个由非常简陋但有用的 2n2222 驱动的扬声器中播放。[Thanassis]的网站充满了太复杂的细节，不能在这里张贴，但太整洁，不能错过。观看休息时间下方的视频进行演示。

当然，ATtiny85 是一个微小但方便的小生物。你可能会喜欢看到它被用作游戏控制台，甚至是 T2 频谱分析仪。你有自己的 ATtiny85 hack 想分享吗？请务必通过[热线](https://hackaday.com/submit-a-tip/)让我们知道这件事！

 [https://www.youtube.com/embed/B6dVIQt_cSE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B6dVIQt_cSE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

