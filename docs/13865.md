# 毁灭战士的 Linux 发行版

> 原文：<https://hackaday.com/2022/06/09/a-linux-distribution-for-doom/>

如果你比 Ubuntu 或 Fedora 之类的标准桌面发行版更深入地了解 Linux 世界，你无疑会遇到一些更有针对性的发行版。一些例子是 Kali 用于安全测试，DragonOS 用于软件定义的无线电，或者 Hannah Montana Linux 用于某些音乐爱好者。任何人都可以用合适的工具推出他们自己的 Linux 发行版，包括[Shadly]，他最近创建了一个[，它只装载了足够启动 1993 年经典*毁灭*的软件。](https://github.com/shadlyd15/DoomLinux)

发行版尽可能简单，除了启动游戏所需的内容之外，不会增加任何负担。它通过 BusyBox 加载 Linux 内核和标准实用程序，然后运行 [fbDOOM](https://github.com/maximevince/fbDOOM) ，这是游戏的一个端口，专门设计为在 Linux framebuffer 上运行，具有最小的依赖性。在这之后，剩下的唯一事情就是使用 GRUB 来启动发行版，并且只需一会儿，Doomguy 就可以开始杀死恶魔了。整个发行版放在一个可引导的 ISO 文件中，该文件可以放在任何可引导的驱动器上。

至于*DOOM*hacks，我们习惯于看到游戏运行在它从未打算运行的硬件上，如[的 NES](https://hackaday.com/2019/06/06/doom-on-the-nes/)或[的办公室电话](https://hackaday.com/2021/08/13/doom-on-a-desk-phone-is-just-the-tip-of-the-iceburg/)。另一方面，这个版本让我们更深入地了解了一个成熟的 Linux 发行版需要多少东西，只要您需要做的事情相对简单。

 [https://www.youtube.com/embed/VaALEKWQOpg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VaALEKWQOpg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

