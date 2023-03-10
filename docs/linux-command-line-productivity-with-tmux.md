# 使用 Tmux 提高 Linux 命令行效率

> 原文：<https://hackaday.com/2020/05/01/linux-command-line-productivity-with-tmux/>

众所周知，大多数 Linux power 用户使用 shell 来完成许多任务，对于那些知道自己在做什么的人来说，这是非常高效的。此外，有一些任务只能从命令行执行，尽管它们的数量每年都在减少。然而，这些天我们被宠坏了，因为你可以有一个 X 会话同时运行许多终端。如果你登录到一个服务器，它可能没有 X。或者你可能通过一个慢速连接登录到一台计算机，在那里使用 X 是很痛苦的。然后呢？现代的答案是 tmux 终端多路复用器，并且[zserge]对如何在命令行使用 tmux 来提高效率进行了深入的介绍。

特别是，他分享了一些配置并提供了合理的建议。例如，你真的需要一个状态栏来显示你的 CPU 负载吗？很酷，是的，但并不总是实际的胜利。

传统的答案是使用屏幕。这是一个古老的程序，它允许您做与 tmux 几乎相同的事情，但是新程序有几个优点:

*   tmux 程序更容易配置
*   您可以更容易地通过脚本来命令 tmux
*   tmux 中的 Unicode 支持更好

另一方面，screen 非常成熟，而 tmux 相对较新。尽管如此，tmux 并不新鲜，而且对许多人来说工作得很好。

如果你想要更多的功能，试试 byobu，它可以使用 screen 或 tmux 来完成实际的工作，无论你喜欢哪个。我们甚至在过去简单地讨论过所有三个项目。说到在终端工作，我们发现有趣的是，我们现在可以在 Windows 上运行一个相当好的版本的 [bash，在 Linux 上运行 Powershell](https://hackaday.com/2016/08/30/shell-game/)。