# 电子书阅读器，但只是为了俳句

> 原文：<https://hackaday.com/2021/02/18/an-e-book-reader-but-just-for-haiku/>

电子墨水显示器并没有彻底改变世界，而是在 Kindle 等电子书阅读器中谦逊地为我们服务。大多数这样的阅读器是为长时间阅读小说之类的东西而设计的，但[Roni Bandini]认为俳句大小的设备是合适的。

这款小巧的设备使用 ESP32，它有足够的时钟周期来轻松驱动显示器。它配有一个 2.9 英寸的 Waveshare 电子墨水显示屏，可以用流行的日本俳句格式来表达诗歌——5 音节，7 音节，5 音节。使用[GxEPD 库](https://github.com/ZinggJM/GxEPD)向显示器写入很容易，它与各种常见的电子墨水显示器兼容。目前，诗歌是硬编码在程序中的，ESP32 宽敞的程序存储中可以包含很多内容。然而，[Roni]指出，让读者从 SD 卡中提取诗歌会很简单。

这是一个有趣的项目，也是熟悉使用电子墨水显示器的基础知识的好方法。我们希望看到一个支持 WiFi 的版本，也能从网上下载最热门的日常俳句。有趣的是，我们自己的档案中只有另一个与著名的日本艺术有关的特征[，它与诗歌几乎没有关系。如果你想改变这一点，做一些相关的东西，然后](https://hackaday.com/2009/08/13/tatjana-van-vark/)[给我们写封短信](http://hackaday.com/submit-a-tip)。休息后的视频。

 [https://www.youtube.com/embed/rBlDi_jEWQs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rBlDi_jEWQs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

