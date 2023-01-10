# 35C3:高级语言中的安全驱动程序

> 原文：<https://hackaday.com/2018/12/31/35c3-safe-and-secure-drivers-in-high-level-languages/>

编写设备驱动程序总是进入 Linux 内核代码之旅的良好开端。当然，内核是一个高度复杂的软件，如果你把代码弄乱了，你可能会拖垮整个系统。另一方面，用户空间驱动可能在你的简历上看起来不太好，但是它们可以帮助你避开内核空间的一些危险和复杂性。此外，您不必将自己局限于 C 语言来编写它们，尤其是如果您担心常见的 C 语言陷阱以及它们可能导致的安全问题。

考虑到这一点，【保罗·埃梅里希】正在研究[使用其他高级语言的英特尔 10Gbit 网卡的 Linux 用户空间驱动程序的概念](https://media.ccc.de/v/35c3-9670-safe_and_secure_drivers_in_high-level_languages)，并招募他的学生撰写关于尽可能多的语言的实现细节的最终论文。

在去年的 34c3 上，[Paul]已经[展示了为 Linux](https://hackaday.com/2018/01/01/34c3-roll-your-own-network-driver-in-four-simple-steps/)编写这样一个用户空间网络驱动程序的基础知识，现在它已经成为他的学生们的参考实现。我们在这里不会看到 Bash 或 JavaScript，但我们将看到一个简短的总结，它通常意味着用 C#、Swift、OCaml 或 Haskell 开发用户空间驱动程序，以及[塞巴斯蒂安·伏伊特]和[西蒙·埃尔曼]关于 Go 和 Rust 的更详细的见解。每种语言的实现[的集合可以在 GitHub](https://github.com/ixy-languages/ixy-languages) 上找到。

由于其中一些语言自带内存处理并执行不可预测的垃圾收集，因此性能和延迟是这里要讨论的两大主题。但是，总的概念是独立于语言的，所以即使世界上没有任何东西可以让你放弃 C，你至少可以带走一些驱动程序开发的新想法。

 [https://www.youtube.com/embed/aSuRyLBrXgI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aSuRyLBrXgI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

