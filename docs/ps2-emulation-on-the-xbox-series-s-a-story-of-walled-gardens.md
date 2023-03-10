# Xbox 系列上的 PS2 模拟:围墙花园的故事

> 原文：<https://hackaday.com/2020/12/15/ps2-emulation-on-the-xbox-series-s-a-story-of-walled-gardens/>

在这一点上，这几乎不再是一个秘密，今天来自微软和索尼的游戏控制台本质上是 AMD 的游戏装备，打包成一个定制的包，并带有调整的系统软件。因此，尽管微软试图阻止，大胆的黑客在 Xbox Series X|S 游戏机上运行 RetroArch 的 Playstation 2 模拟器也就不足为奇了。(视频，嵌在下面。)

通过支付 19 美元[购买一个微软开发者账户](https://arstechnica.com/gaming/2020/11/how-to-turn-your-xbox-series-x-s-into-an-emulation-powerhouse/)，在 XBox 主机上设置开发者模式，并从官方网站获得 RetroArch 的通用 Windows 平台( [UWP](https://en.wikipedia.org/wiki/Universal_Windows_Platform) )端口，可以偷偷通过微软的安全检查点。这种方法的优势在于它受到了雷德蒙神的保佑。但是由于 2 GB 的限制，人们不能在开发者模式下玩零售游戏和大型游戏。

最近，一个名为[tunip3] [的黑客在 Xbox 应用分发系统中发现了一个漏洞](https://arstechnica.com/gaming/2020/11/how-one-developer-is-sneaking-emulators-through-a-hole-in-the-xbox-store/)，它允许人们下载 RetroArch 的“零售”版本。这包括将 RetroArch 应用程序标记为“私有”，允许它跳过微软的审查。电子邮件地址在白名单上的人将被授予在 Xbox 主机上下载该应用程序的权限。这种“零售”方法的优势在于它没有 2 GB 的文件大小限制。缺点是微软可以随意撤下该应用并封禁[tunip3]的开发者账号。

## 我的路对公路

很多事情都可以归结为一个简单的问题“为什么？”。为什么要跨越这些障碍，在最终运行 Windows 10 的游戏 PC [上设置一个有限的、可能会破坏 ToS 的模拟器呢？为什么不使用树莓 Pi 4 或 NUC 系统，过去几个月里，它一直被塞在一个布满灰尘的角落里，给你带来悲伤的眼神？](https://en.wikipedia.org/wiki/Xbox_system_software#Xbox_One_and_Xbox_Series_X_and_Series_S)

根据其硬件规格，Playstation 5 应该能够播放从最初的 PSX 到 PS4 的任何 Playstation 游戏，但它只提供对 PS4 的兼容性。另一方面，XBox Series X|S 在 XBox 游戏的整个谱系中提供了这样的向后兼容性，尽管没有包括为微软主机发布的每一款游戏。

[![](img/bfacf6509430c8364844d27e4771b2c1.png)](https://hackaday.com/wp-content/uploads/2020/12/xbox-one-x-s-playing-PS2-God-of-War.jpeg)

Xbox One S playing PS2 version of the original God of War

任天堂与运行他们自己的受祝福的模拟器解决方案有着分分合合的关系，例如用于 Wii、Wii U 和 3DS 的[虚拟控制台](https://en.wikipedia.org/wiki/Virtual_Console) (VC)，它甚至为非任天堂游戏提供游戏访问。然而，在 2019 年初，任天堂开始逐步淘汰风险投资。在许多方面，风投服务是最接近 RetroArch 今天所提供的服务，即使人们可能会对风投上有限的游戏数量和购买游戏权利的每场游戏费用有所争议。

所有这些都使人想知道，如果像 VC 这样的多系统仿真服务，但具有更大的游戏库和更低的成本(例如，作为 PSN 订阅的一部分，完全访问)将会发生什么。这足以让人们停止尝试在他们全新的游戏机上进行追溯吗？

## 它叫做个人电脑

怀疑论者对这件事的看法可能是，随着这些天视频游戏控制台缺乏真正独家的标题，人们还不如在电视下面贴一个自己选择的 SFF 钻机，运行自己最喜欢的操作系统，并由自己选择的控制器控制。使用 Steam 的[大画面](https://store.steampowered.com/bigpicture)功能或等效功能，用一个控制器控制它就像是一个专用的游戏控制台一样容易。

在这个游戏平台上安装 retrach 和类似的东西也是轻而易举的事情，并且可能对更多的模拟器更好，因为它是一个标准的 Windows 或 Linux 系统，retrach 实际上是针对这个系统优化的。让我们再次回到为什么人们试图用困难的方式做事。

游戏机和其他围墙花园的巨大吸引力通常是“它就是工作”的卖点。买下来，设置好，开机，开始玩游戏，不用担心。不是每个人都喜欢在 Windows 上调试模糊的兼容性和驱动程序问题，或者弄清楚为什么在 Linux 上启动游戏会导致 Xserver 崩溃。从这一点来看，让它做得更多一点很有吸引力，至少对那些甚至在孩提时代就发现自己盯着设备、感觉手指有那种熟悉的痒感的人来说是如此。

归根结底，这本质上只是爱好和兴趣的问题。即使微软等公司强烈反对，如果有人黑掉他们的 PS5 或 XSX，在上面运行额外的软件，给这些硬件的所有者带来更多的乐趣，也没有人会受到伤害。毕竟，大多数有趣的黑客都是这样诞生的。

实用吗？不会吧。好玩吗？你打赌。

 [https://www.youtube.com/embed/psTunlgKOMM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/psTunlgKOMM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

