# 井字游戏，在 TTL 中

> 原文：<https://hackaday.com/2019/06/29/tic-tac-toe-in-ttl/>

我们都熟悉井字游戏，或称“画圈画叉”,这是一种童年纸笔游戏，已经成为许多编码练习的基础。这是一个很容易用软件实现的任务，但是我们中有多少人见过只用硬件实现的呢？这正是[Warren Toomey]使用 TTL 芯片所做的，他的方法使电路出奇的简单。

它的核心是一个 8 kB 的 ROM，包含预先计算的移动序列，这些序列是通过由玩家和机器的游戏状态组成的地址选择的。一系列的触发器控制和按钮，使董事会，和 555 提供了一个时钟。

使用 ROM 取代复杂逻辑的技术是一种非常强大的技术，这得益于曾经难以负担的相对较大器件的低价位。我们已经在其他地方看到了这种技术，包括将[作为 TTL CPU](https://hackaday.com/2019/06/15/a-ttl-cpu-minimising-its-chip-count) 中的 ALU，甚至对于[来说，一个完整的 CPU 拥有自己的权利](https://hackaday.com/2017/02/02/the-gray-1-a-computer-composed-entirely-of-rom-and-ram/)。

你可以在下面的视频中看到操作的结果，如果你想亲自尝试，可以在 GitHub 库中找到所有相关信息[。](https://github.com/DoctorWkt/TTL_TicTacToe)

 [https://www.youtube.com/embed/WPPjL46z-Ag?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WPPjL46z-Ag?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

