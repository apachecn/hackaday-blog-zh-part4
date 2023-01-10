# 厌倦了爆米花？改为烘焙咖啡

> 原文：<https://hackaday.com/2021/02/25/tired-of-popcorn-roast-coffee-instead/>

这些年来，我们已经看到了很多咖啡烘焙机。本·伊根从一台热气爆米花机开始了他的事业。如果你认为这就像用豆子代替爆米花一样简单，那就再想想吧。你需要很好地控制热量，这需要一些温度监测和控制器——在这种情况下，一个 Arduino。下面的[Ben 的]视频展示了这一切是如何进行的。

Arduino 和电源绑在两侧，看起来有点像糟糕的后启示录电影中的东西。但看起来它完成了任务。

除 Arduino 外，热电偶还测量温度，这需要一个 MAX31855 形式的小电路。还有一个继电器来开关加热器。当然，还有其他控制交流电源的方法，如果继电器冒犯了你的感受，你可以选择固态继电器。

唯一的另一个问题是增加了一个额外的电源，这样风扇可以在没有加热器的情况下运行。可能有一些其他的方法来管理这一点，但电源足够便宜，至少捆绑的电源可以抵消 popper 另一侧 Arduino 上的捆绑。

当然，我们以前见过像这样使用的爆米花机。热电偶是测量高温的一个很好的方法，但是还有很多其他的方法来测量这个特殊的量。

 [https://www.youtube.com/embed/jouKJEVmwRQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jouKJEVmwRQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

