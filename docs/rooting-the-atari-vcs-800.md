# 扎根雅达利 VCS 800

> 原文：<https://hackaday.com/2021/07/27/rooting-the-atari-vcs-800/>

雅达利 VCS 800 是一款现代产品，是个人电脑和游戏机的混合体。从根本上说，它是一个运行 Linux 的盒子里的一堆现代芯片，可以让你浏览网页或模拟一些旧游戏。现在，多亏了[ArcadeHustle]，[你可以在闲暇时对 VCS 800 进行持久的根访问。](https://github.com/ArcadeHustle/AtariVCSroot)

诀窍很简单，从在引导时中断 systemd 启动脚本开始。然后，用户可以将文件合并到/etc 目录中，通过 tty 终端或 TCP 实现根用户访问。这些都包含在上面 Github 链接中的脚本中。

你实际上可以在硬件上运行各种操作系统，因为它由 AMD 锐龙 R1606G CPU 驱动，运行简单的 PC 架构。然而，如果你想定制现有的操作系统来满足你的要求，这种方法是可行的。

如果你想在系统上有所作为，获得 root 访问权限是关键。我们已经在[瘦客户端](https://hackaday.com/2015/04/29/hacking-a-thin-client-to-gain-root-access/)以及[汽车信息娱乐系统](https://hackaday.com/2021/01/30/nissan-gives-up-root-shell-thanks-to-hacked-usb-drive/)上看到了这种做法，让车主完全控制他们所拥有的硬件。如果你有自己的 root exploit 想要分享，请给我们写信，[好吗？](http://hackaday.com/submit-a-tip)