# 晨风在你不注意的情况下重启了原来的 Xbox

> 原文：<https://hackaday.com/2021/04/14/morrowind-rebooted-the-original-xbox-without-you-ever-noticing/>

最初的 Xbox 以基于基本的 PC 硬件而闻名，在开发人员中，以只有 64 兆内存而闻名，即使在当时这也不是很多。在最近的播客中，Bethesda 的[Todd Howard]讲述了那个时代的一件轶事，声称*morrow wind*偶尔会在用户不知情的情况下无形地重启 Xbox，以释放 RAM。【现代复古游戏玩家】想要确定这是真是假，[于是开始了调查。](https://www.youtube.com/watch?v=x0TKwPnHc-M)

调查从 Xbox 开发工具包的帮助开始。注意，最初的轶事提到了在加载过程中发生的重启，devkit Xbox 在执行加载后被软重启。它没有回到游戏的标题屏幕，而是直接踢回了加载屏幕，转而调出了上次保存的游戏。这表明游戏确实能够在加载过程中重启。

[Modern Vintage Gamer]有一种预感，这是通过使用一个名为 XLaunchNew Image 的例程实现的，这是 Xbox API 的一部分，可用于软启动控制台并启动可执行文件。在反编译*morrow wind，*之后，找到了一个符合要求的调用。进一步的分析表明，该游戏在加载和启动新游戏时确实调用了 XLaunchNewImage，并通过找到一个*得到了确认。包含启用此行为的标志的 ini 文件。

据推测，这种行为的原因是加载保存时重新启动游戏比试图从当前游戏中卸载内存中的所有游戏资产更简单。这是一个巧妙的技巧，一旦开发团队实现了它，他们的生活可能会变得容易得多。

我们在这里很少谈论*上古卷轴*系列，[虽然我们看到有人改装了一辆健身车来配合 *Skyrim。*](https://hackaday.com/2016/07/09/staying-in-and-playing-skyrim-has-rarely-been-this-healthy/) 视频中断后。

 [https://www.youtube.com/embed/x0TKwPnHc-M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/x0TKwPnHc-M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

