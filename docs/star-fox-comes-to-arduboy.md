# 星狐来到阿杜博伊

> 原文：<https://hackaday.com/2019/01/07/star-fox-comes-to-arduboy/>

最初的 SNES 星狐是一款里程碑式的游戏。凭借内置在盒式磁带中的 Super FX 芯片，它提供了第一个 3D 加速家用控制台体验。该系列跨越了几个控制台和二十多年。现在，多亏了[夏羽·霍肯赫尔]，它有了一个通往阿都博伊的港口(尽管是非正式的)。

令人印象深刻的是，这款游戏的大小不超过 28KB，而且[夏羽]在开发细节上也毫不吝啬。这个过程从在 Arduboy 上设置一个基本的 3D 引擎开始，然后是对各种游戏创意的一些测试。最终的实现与最初的 SNES 游戏非常相似。在这一点上，工作从 Arduino IDE 转移到了[夏羽]的定制开发环境中，以加快进度。PC 端口用于节省每次迭代编程 flash 的时间。

实现这一目标的技巧多种多样。有整洁的黑客用来优化 3D 模型数据的存储，实现轻量级碰撞检测，并生成随机级别。一切都是为了让游戏尽可能地适应最小的空间。

在 16MHz 8 位微控制器上运行流畅的 3D 图形是一个令人印象深刻的壮举，也是对[夏羽]编码能力的证明。我们迫不及待地想看到平台上更多的 3D 开发。同时，如果 Arduboy 没有你想要的样子，也有一个解决办法。休息后的视频。

 [https://www.youtube.com/embed/ES3fGLuse4s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ES3fGLuse4s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

