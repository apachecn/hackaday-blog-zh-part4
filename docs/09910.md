# 七个玩家能在一台 1996 年的 SGI 机器上玩《雷神之锤》吗？

> 原文：<https://hackaday.com/2021/05/01/could-seven-gamers-play-quake-on-just-one-1996-sgi-machine/>

几年前进行了一项有趣的实验。通过在一台具有大量 RAM 和 GPU 的塔式 PC 上运行多个虚拟机，可以让七名游戏玩家同时在一台设备上玩游戏。[CelGenStudios]发现这个想法很有意思，并从理论上认为同样的壮举可能在 20 世纪 90 年代中期的硅图形硬件上实现。

这个想法是使用 Origin 2000 服务器作为基础。这些产品没有任何形式的视频输出，甚至没有键盘和鼠标接口。然而，通过替换 Onyx2 机器上的 IO6G 模块和 Octane 上的 SI 图形卡，可以让图形和输入正常运行。通过一个名为“鞋盒”的 PCI 适配器安装多个显卡和几个 CAD DUO 板，可以提供多达四个独立的显示器、键盘和鼠标。有了所有这些硬件，理论上可以让四个用户登录 Origin 2000 机器上运行在 IRIX OS 中的 X 服务器。然后，只需启动四个 *Quake* 实例和一个专用服务器，你就可以开始游戏了。

[CelGenStudios]甚至探索了超级计算机级硬件的极限，表明 7 个或更多玩家是可能的。不幸的是，SGI 硬件并不容易获得，也不便宜，即使在发布几十年后也是如此——到目前为止，这个概念仍然未经测试。我们非常希望看到这样的设置发生在 *QuakeCon* 或者黑客大会上，所以如果你成功了，[你知道怎么打电话给](http://hackaday.com/submit-a-tip)。我们注意到[在吉姆·奥斯汀电脑收藏馆](http://www.computermuseum.org.uk/news.html)有一些辛烷 2000，所以它们可能是实现这一壮举的人。

同时，通过最初的[Linus Tech Tips]项目，查看现代硬件概念的实践探索。基本理论很简单——制造一台功能强大的电脑，配备强大的 CPU、充足的内存，并为七名玩家每人配备一块显卡。他们运行多个虚拟机，并设法在仅运行一个 CPU 的情况下提供完整的 7 人游戏体验。

 [https://www.youtube.com/embed/LXOaCkbt4lI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LXOaCkbt4lI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

