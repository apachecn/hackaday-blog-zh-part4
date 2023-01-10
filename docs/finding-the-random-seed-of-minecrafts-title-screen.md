# 寻找《我的世界》标题屏幕的随机种子

> 原文：<https://hackaday.com/2020/07/20/finding-the-random-seed-of-minecrafts-title-screen/>

《我的世界》是一款探索程序生成世界的游戏。每个世界都是由特定的“种子”值生成的，共享这个种子值可以让其他人在自己的游戏中生成相同的世界。最近，分布式计算项目《我的世界》@Home 开始尝试寻找《我的世界》标题屏幕中显示的世界的种子值，并且已经成功实现了他们的目标。

不应低估完成这项任务所需的工作量。137 名用户贡献了 181 台主机和 231 个 GPU，在不到 24 小时内找到了解决方案。该项目的捐助者名单很长。似乎找到种子的方法包括将不同种子世界的截图与原始图像进行比较。这需要大量的逆向工程来计算相机 FOV 和原始拍摄的其他设置，以便可以准确地比较结果。有趣的是，该小组发现了两个可以生成必要世界的种子，这表明世界生成器代码在种子值之间存在一些冲突。

我们不确定哪个更令人震惊，是投入到项目中的工作量，还是有一个分布式计算项目在处理先进的《我的世界》研究。不管怎样，我们对这些地区的《我的世界》黑客并不陌生。休息后的视频。

 [https://www.youtube.com/embed/caLCZNLPgrM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/caLCZNLPgrM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/GaRurhiK-Lk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GaRurhiK-Lk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

