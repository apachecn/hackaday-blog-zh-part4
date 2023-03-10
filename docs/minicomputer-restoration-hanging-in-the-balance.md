# 小型机修复悬而未决

> 原文：<https://hackaday.com/2022/03/20/minicomputer-restoration-hanging-in-the-balance/>

[大卫·洛维特]又名天兔电气公司花了几个月的时间解剖一台 1980 年的百夫长小型计算机。他的最新更新显示[修复遇到了一些障碍](https://www.youtube.com/watch?v=l8-P_-9KrgU)，启动这个古老的蓝色怪兽将是一个挑战。

当我们最后一次检查这个项目时，[David]已经建立了一个[自制 ROM 阅读器](https://hackaday.com/2021/08/10/homebrew-rom-reader-saves-data-from-a-vintage-minicomputer/)来备份存储在几个小型机 ROM 芯片上的关键数据。从那以后，好消息是百夫长有了生命迹象。探测默认 RS232 串行端口上的数据集就绪引脚会发现一个数据流，可能来自“CPU6”板。

不幸的是，好消息到此为止。将一个终端添加到串行端口会中断该数据流，并且在测试的三个终端中没有任何一个发送或接收信息。更糟糕的是，这两个巨大的硬盘似乎都在 20 世纪 90 年代的某个时候遭受了灾难性的磁头崩溃，在这个过程中摧毁了 Centurion 操作系统和其他可能的重要数据。污染的空气过滤器可能是罪魁祸首，有证据表明年度维护被忽视了。虽然至少有一个驱动器可以用新的盘片修复，但原始操作系统会完全丢失。

幸运的是，百夫长的一名前雇员能够提供大量未记录的信息，这些信息极大地有助于理解小型计算机的各个组件。令人难以置信的是，他们还能够为百夫长系统提供 PROM 诊断板。该板不仅可以运行一系列测试，还可以用 TOS(测试操作系统)引导系统，TOS 是存储在卡的 PROMs 中的一种基本内存监视器。虽然诊断卡本身需要修复，但现在有一点点机会[大卫]可以使用 TOS 作为为百夫长编写新软件的起点。

我们真的迫不及待地想看看这个项目接下来会发生什么。我们过去报道过一些非常特殊的老式电脑修复，比如来自罕见的施乐奥拓的[被诅咒的暗黑驱动器](https://hackaday.com/2018/05/10/diablo-drive-appears-to-be-cursed/)，更不用说原始苹果 1 的微妙的[加电程序了。](https://hackaday.com/2022/01/10/powering-up-an-original-apple-i-after-three-decades-in-a-museum/)

 [https://www.youtube.com/embed/l8-P_-9KrgU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/l8-P_-9KrgU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

