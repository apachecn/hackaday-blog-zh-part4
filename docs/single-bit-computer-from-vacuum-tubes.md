# 真空管单比特计算机

> 原文：<https://hackaday.com/2021/12/27/single-bit-computer-from-vacuum-tubes/>

历时一年的项目达到高潮，[天兔电气]又名[大卫]刚刚完成他的[单比特真空管计算机](https://hackaday.io/project/181923-1-bit-vacuum-tube-computer)。它基于[摩托罗拉 MC14500 1 位工业控制器](http://ww.bitsavers.org/components/motorola/14500/MC14500B_Rev3.pdf)，但是由于【大卫】将基本逻辑单元改为算术逻辑单元，他将其命名为 **UE14500** 。建在约 2.5 x 3 兔长的木板上，不包括电源。[David]承认他有一点欺骗，因为他在计算机所基于的通用或非门中使用了两个硅二极管，而不是 6AL5 双二极管管——但他在辩护中指出，那个时代的许多真空管计算机都使用硅二极管。

![](img/606afb60301a704f26c5937952871baf.png)

他在或非门中使用的电子管是 6AU6 微型五极管，他选择这种电子管是因为它的可用性、价格和低压适用性。[David]使用+24 和-12 VDC 两种电源运行这台计算机，而不是真空管设计中通常使用的数百伏电源。模块构建在使用铣床蚀刻的单面覆铜 PCB 板上。休息时间下面的视频总结了这个 22 集的系列，其中他解决了一些电源问题，并为 I/O 构建了一个远程前面板，并演示了计算机的运行。唉，这仅仅完成了项目的四分之一，因为在整个系统完成之前，还有三个构建模块要构建——程序控制(磁带)、ram 内存条和串行输入/输出模块。我们期待着看到整个系统在未来启动和运行。

几天前我们刚刚写了关于 MC14500 的文章，我们还报道了[大卫]的[555 定时器的真空管实现，以及他的其他真空管项目，其中几个在](https://hackaday.com/2021/03/28/should-have-used-a-vacuum-tube-555/)[他的 Hackaday.io 页面](https://hackaday.io/usagi.electric)上有介绍。

 [https://www.youtube.com/embed/q9oB-6963DU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q9oB-6963DU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

