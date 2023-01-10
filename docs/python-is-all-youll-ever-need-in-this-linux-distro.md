# Python 是你在这个 Linux 发行版中所需要的一切

> 原文：<https://hackaday.com/2020/06/01/python-is-all-youll-ever-need-in-this-linux-distro/>

选择满足您个人需求和喜好的完美 Linux 发行版可能是一项不可能完成的任务，并且常常需要一点斯德哥尔摩综合症的暗示作为妥协。在极端的情况下，你可能最终只是推出自己的发行版。虽然挫折总是改变的巨大动力，但对[乔希·摩尔]来说，是好奇心和好玩的兴趣让他创建了 [snakeware，一个 Linux 发行版，其中整个用户空间不仅运行在 Python 上，而且*是* Python](https://github.com/joshiemoore/snakeware) 。

想象一下，你将启动你的 Linux 系统，而不是你选择的 shell，迎接你的将是一个交互式 Python 解释器，你在系统上所做的一切都将在这个解释器的范围内——这就是 snakeware 的要点。现在，这可能一开始听起来相当有限，但请记住，我们在这里谈论的是 Python，这是一种以其多功能性而闻名的语言，有大量的包可以快速轻松地完成事情，这正是[Josh]的目标。为了了解这一点，snakeware 还包括了 *snakewm* ，这是一个用 pygame 编写的图形用户界面，捆绑了几个简单的应用程序作为演示，包括一个执行 Python 一行程序的终端。

请注意，在这个阶段这仅仅是一个概念的证明，但是[Josh]正在邀请每个人来贡献和扩展他的创作。如果您想尝试一下而不构建整个系统，[GitHub 存储库有一个预构建的映像](https://github.com/joshiemoore/snakeware/releases)可以在 QEMU 中运行，窗口管理器也可以作为常规 Python 应用程序在您的普通系统上运行。为了快速浏览一下，请在休息后观看演示视频。

当然，死忠的 Linux 爱好者很难接受一个没有他们最喜欢的 shell 和最喜欢的语言的发行版，但是，嘿，至少没有 [systemd](https://hackaday.com/2019/10/16/pack-your-bags-systemd-is-taking-you-to-a-new-home/) 它也能过。虽然 snakeware 在不久的将来可能不会与更成熟的发行版竞争，但它肯定是一个有趣的概念，包含了跳出框框思考和尝试不同的东西。它绝对适合[写在名片上](https://hackaday.com/2019/12/24/now-even-your-business-card-can-run-linux/)。

 [https://www.youtube.com/embed/Zy8NXuzBPhA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Zy8NXuzBPhA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

