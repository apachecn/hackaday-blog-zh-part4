# 断路器是如何断开的？

> 原文：<https://hackaday.com/2021/01/26/how-does-a-circuit-breaker-break/>

即使你不是一个电子人，你可能有断路器的工作知识。当灯熄灭时，你找到断路器，把它弹回到开的位置。大多数人也明白，如果你插了太多东西或者意外短路而使电路过载，断路器就会跳闸。但是这种常见的设备实际上是如何工作的呢？请记住，断路器需要超级可靠，并且已经存在足够长的时间，你可以想象它们是相当低的技术。[学习工程]有一个非常清晰的视频，讲述了断路器内部发生的事情，值得观看八分钟。你可以看下面的视频。

手柄是一个机械工程奇迹，使用了两个弹簧和一个特殊的设计，即使很小的力也会使它迅速关闭。有人绊倒了它。然而，你还有另外两种情况需要关闭它:过载和短路。

短路情况很容易用电磁铁检测到，当这么大的电流流过时，电磁铁会产生很强的磁场。然而，超载的情况并没有那么突然。为此，断路器使用双金属线圈，它受热时会膨胀。

还有一个细节。当断路器在高电流下断开时，会形成电弧。里面有一种特殊的成分可以帮助消除电弧。那个小盒子里发生了很多事情。

当然，现在有更好的断路器可以检测电弧、短路和过载。在过去，我们也至少见过另外一个[断路器拆卸](https://hackaday.com/2016/02/26/inside-a-circuit-breaker-with-mikeselectricstuff/)。

 [https://www.youtube.com/embed/v7XztOokA9Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/v7XztOokA9Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

