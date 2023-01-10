# 你有老鼠！

> 原文：<https://hackaday.com/2020/08/01/youve-got-rat/>

如果你的家从未遭受过鼠患，那么你是幸运的。我们的世界充满了老鼠，尽管人类尽了最大的努力来控制它们，但还是不可避免地有一些会找到出路。对马里乌斯·塔丘克来说，这成了一个问题，因为他的捕鼠器需要经常检查，以避免老鼠尸体腐烂。他的解决方案？配备有 ESP8266 的人道陷阱，当啮齿动物被监禁时会通知他。

它背后的技术是尽可能简单的，陷阱的门启动一个开关，启动一个 ESP8266 模块。ESP 的代码只是唤醒它，连接到无线网络，并向 IFTTT 发送一个查询，同时调用一个向他发送电子邮件警报的服务。不需要监控任何 GPIO 线路或运行任何代码来监视陷阱，这完全是电源开关的功能。

这个陷阱本身很有趣，因为它是一个由焊接铜线制成的自制陷阱。遗憾的是，它的构造细节很少，但你可以在下面的视频中看到更多，包括里面的一只活老鼠。如果你对制作陷阱感兴趣，[我们可以帮你](https://hackaday.com/2016/05/20/a-better-mousetrap-at-least-for-the-mouse/)。

 [https://www.youtube.com/embed/lBcRwNkVIK4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lBcRwNkVIK4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

