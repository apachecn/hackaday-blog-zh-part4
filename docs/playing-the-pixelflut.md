# 演奏 Pixelflut

> 原文：<https://hackaday.com/2020/08/01/playing-the-pixelflut/>

每次黑客聚会都需要尽可能多的像素。找一群人在一起，你会被展示的光量弄得眼花缭乱。(我们建议用“一盏闪光灯”作为这一类群的分类名称。)在大型聚会上，有什么比“比赛”谁能画出最好的 LED 画布更好的方式来展示您的精英黑客能力呢？进入 [Pixelflut，多人绘图画布](https://github.com/defnull/pixelflut)。

Pixelflut 至少从 2012 年的[就已经存在了，但是在编辑【Jenny List】在她的](https://cccgoe.de/w/index.php?title=Pixelflut&oldid=4792)[对 SHA 2017](https://hackaday.com/2017/08/25/shacamp-2017-a-personal-review/) 的评论中提到它之后，它引起了作者的注意。中央酒吧后面的娱乐表演是什么？原来是运行 Pixelflut 的服务器驱动的显示器。Pixelflut 服务器展示了一个显示器，可以通过以极其简单的协议在网络上发送命令来绘制该显示器。每个服务器只支持四个 ASCII 命令——基本上是 get pixel、set pixel、screen size 和 help——所以实现客户机或服务器都是轻而易举的事情，这就是要点。![](img/20dbaeab4fd3b9fd25fe985c856ebd5f.png)

虽然最初的实现看起来是由顶部链接的[defnull]编写的，但在某种意义上，Pixelflut 更像是一个通用协议，而不是一个实现。从某种意义上说，一个人“玩”的是各种 Pixelflut 迷你游戏中的一个。当一个共享空间中有一个显示器时，游戏是谁可以通过最快的绘制来控制最大的区域，要么是聪明，要么是消耗尽可能多的带宽。

然后是一场游戏，看谁能写出最快的、久经沙场的服务器，以便在不崩溃的情况下处理所有的流量。为了给人一种规模的感觉，36c3 的一个[装置报告](https://twitter.com/C3Pixelflut/status/1211669392808910848)说，一个真正庞大的 0.5 *千兆字节*的数据以超过 30 千兆比特/秒的峰值速率消耗，仅仅是画像素！除了最灵活的服务器实现之外，这注定会使所有的实现陷入困境。(“Flut”在德语中是“洪水”。)

虽然黑客阵营在可预见的未来可能会暂停，但编写一个高性能的 Pixelflut 客户端或服务器似乎是一个在我们等待他们回归的同时提高个人技能的绝佳方式。如需视频示例，请查看休息后的嵌入。有喜欢的实现吗？在评论中告诉我们吧！

> 用 [#Python](https://twitter.com/hashtag/Python?src=hash&ref_src=twsrc%5Etfw) 在 [#33c3](https://twitter.com/hashtag/33c3?src=hash&ref_src=twsrc%5Etfw) 处 70Mbps 接管 [#pixelflut](https://twitter.com/hashtag/pixelflut?src=hash&ref_src=twsrc%5Etfw) 。感谢 [@Maschinendeck_](https://twitter.com/Maschinendeck_?ref_src=twsrc%5Etfw) 的设置，非常有趣。[pic.twitter.com/7ea7JBi7H9](https://t.co/7ea7JBi7H9)
> 
> -什么🗿Alberto granzotto(@ vrde)[2016 年 12 月 30 日](https://twitter.com/vrde/status/814908145520807936?ref_src=twsrc%5Etfw)