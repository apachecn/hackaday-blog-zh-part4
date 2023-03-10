# 寂静之声:加速你的视频消费

> 原文：<https://hackaday.com/2020/06/11/the-sound-of-silence-speed-up-your-video-consumption/>

现在有很多有趣的视频内容。然而，不可避免的是，当我们发布一些东西时，会出现一些评论，哀叹视频不是传播技术信息的最有效方式。我们百感交集。有些东西受益于能够看到，例如，一个截屏。有些人喜欢看到教师与班级互动的人际关系，而不仅仅是阅读。但我们会承认，有时一个视频需要更长的时间来观看，尤其是如果它充满了停顿。来自[labmoellertim]的一款工具可以解决这个问题。命令行工具拍摄一段视频，去掉无声的部分。如果您想使用该技术构建自己的工具，也可以将它用作 Python 库。

如果你曾经上过网上课程，加快视频速度以便更快地完成课程是很常见的。这在一定程度上是可行的，但是消除或加快无声间隙意味着你不必“听得更快”当然，你也可以加快视频速度。

该工具可以检测无声内容和有声内容，并且可以执行多种操作。默认情况下，它会将无声部分的速度提高 6 倍。当然，你可以改变任何一部分的速度。你也可以改变音量——大概是静音。它加快了无声部分的速度，这一事实起初令人不安，但看了一会儿后，你会意识到它在许多情况下有助于你理解正在发生的事情。

举个例子，一个麻省理工学院的 Python 讲座(见下面的视频)在 9:45 开始，但是在处理之后不到 8 分钟。不到两分钟的节省听起来并不多，但对于这样一个短片来说，它几乎节省了 19%。一个小时的讲座加起来将近 12 分钟。当然，这很大程度上取决于演讲者和视频的风格。有些视频可能会节省更多时间；其他人更少。

不幸的是，您确实需要本地的视频文件，所以如果您想将它应用到 YouTube 视频，您需要先下载它。这相对容易做到，但它扼杀了在浏览器中观看视频的即时性。

现在，如果我们能跳过[广告](https://hackaday.com/2018/02/13/your-audio-will-be-back-right-after-this-commercial-break/)。话又说回来，[我们最喜欢的一些视频没有文字](https://hackaday.com/2020/03/15/link-coupling-antenna-tuner-wordless-workshop/)，但它们有时会有音乐，这会妨碍工具的工作。

 [https://www.youtube.com/embed/wl7bveY5Ze4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wl7bveY5Ze4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/EaQh9cZ_jrs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EaQh9cZ_jrs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

