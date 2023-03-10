# 这个发现声音的器官是用 Python 和激光切割机制作的

> 原文：<https://hackaday.com/2022/09/25/this-found-sound-organ-was-made-with-python-and-a-laser-cutter/>

一些读者无疑会记得在他们自行车的前叉上系了一张扑克牌，这样当轮子转动时，辐条就会拍打扑克牌。它应该听起来像摩托车，但它不是，但它是很好的，干净的乐趣，与正常的基线相比，它让我们更加讨厌邻居的退休人员，这已经很高了。

[【Garett Morrison】的“咔哒轮风琴”](https://www.garettmorrison.net/posts/click-wheel-organ/)工作原理和轮辐里的卡片差不多，只是轮子多得多，音乐性也强得多。风琴每一个音符都有一个独立的齿轮，所有的齿轮都在一个共同的轴上转动。每个轮子都是由薄胶合板激光切割而成，在其外圆周上有一系列细齿。由 Python 脚本计算的齿的数量决定了当薄簧片被压向纺车时所发出的声音的音高。因为轮子之间的齿数比是固定的，所以只要轮子的速度保持不变，所有的音符就会保持一致。

下面视频中的概念验证表明，速度控制还没有完全实现——同时播放多个音符似乎会增加阻力，足以减慢轮子的速度，并降低所有音符的音高。轮轴上似乎有一个光电断路器来监控速度，所以我们可以想象一个 PID 回路来控制电机速度可能会有所帮助。还有一个更大的发动机，不容易陷入困境。至于声音，我们只能说它肯定是独一无二的——而且，它看起来像是真的会让人喜欢的东西。

 [https://www.youtube.com/embed/PuulRBH9yVw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PuulRBH9yVw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

