# 最新的 Linux–在 486 的软盘上！

> 原文：<https://hackaday.com/2020/07/08/the-latest-linux-on-a-floppy-in-a-486/>

如果你曾经研究过多种形式的 GNU/Linux 操作系统的早期历史，你会读到[Linus Torvalds]为他的基于 Intel 386 的计算机开发了他的第一个内核。尽管 386 架构现在已经过时，但是当前的 Linux 内核仍然可以为其编译，并且许多发行版仍然保留了 i386 分支，以便为后来能够运行 i386 代码的机器提供广泛的兼容性。但是，如果你把一个当前的 Linux 内核放在一台 20 世纪 90 年代早期的软盘上，内存很少，会怎么样呢？[Fozztex] [就是这么做的](https://www.insentricity.com/a.cl/283)，不是 386，而是 486，配备了当时令人印象深刻的 36MB 内存。您可以在休息时间下面的视频中观看它的运行。

一个最新的 Linux 内核很少被编译成像软盘一样小的东西，所以让一个内核从如此古老的介质上启动似乎是一个挑战。尽管使用`tinyconfig` make 选项是可能的，在通过[土著 Linux](http://landley.net/aboriginal/) 找到一个足够小的根文件系统后，一个可引导软盘就创建好了。它并不完全有用，它的唯一目的是看看 Linux 是否能在 486 上看到一个大硬盘，但它仍然是一个 5.6 版本的 Linux 内核，从一台古老的计算机上的软盘启动。再也不要抱怨你的树莓派 Zero 慢了，我们已经走了很长一段路了！

 [https://www.youtube.com/embed/oBeE_z4HTwg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oBeE_z4HTwg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



标题图像— Afrank99 / [CC BY-SA 2.0](https://commons.wikimedia.org/wiki/File:3,5%22-Diskette.jpg)