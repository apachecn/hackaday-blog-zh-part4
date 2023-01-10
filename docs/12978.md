# 旧 Macintosh 的远程桌面乐趣

> 原文：<https://hackaday.com/2022/03/07/remote-desktop-fun-for-your-old-macintosh/>

在过去的几十年里，从任何地方远程访问您计算机的桌面、文件和网络已经实现了远程工作(即“在家工作”)。现代个人电脑对于虚拟网络计算(VNC)来说已经有了足够多的计算负担，但是这又给我们的复古计算社区留下了什么呢？[马尔西奥·特谢拉]用[MiniVNC 覆盖了它，这是一个全新的远程桌面服务器，用于(非常)老式的麦金塔电脑](https://youtu.be/zM_sNItbuhc)。

现在，在你说任何事情之前，ChromiVNC 确实已经存在了一段时间，对于旧的 MAC 电脑来说，它是一个相当不错的远程桌面服务器。然而，MiniVNC 有几个显著的优点，最值得注意的是，MiniVNC 完全兼容 MacTCP。苹果的第一个 TCP/IP 网络栈随 System 6 登陆了 Macintosh 平台。因此，MiniVNC 可以在一些最老的 Mac 电脑上提供远程桌面，包括 Macintosh Plus。

很难夸大这有多酷——标志性的 Macintosh Plus 于 1986 年发布，运行速度为 8MHz，支持最大 4MB 内存。虽然 MiniVNC 的大部分是用 C++编写的，但软件的部分内容(包括 TRLE 编码)必须用 68K 汇编语言手写，以确保良好的性能。MiniVNC 的整个重点是性能和灵活性，其次是准确性，这似乎是一个正确的决定。奇怪的屏幕伪影和错过的更新似乎是合理的权衡，以便在摩托罗拉 68000 处理器上稍微流畅地运行。

新的麦金塔电脑也可以使用这个软件。如果您幸运地拥有 68020 或更高版本的处理器，MiniVNC 软件将利用额外的 CPU 指令来进一步提高性能。每一点都有帮助，因为在这样一个原始的系统上收集屏幕更新是非常耗费资源的。这个项目一点都不简单，从使用回调例程创建循环到记录鼠标按钮状态这样简单的事情。整个项目可以在 GitHub 上找到，其中有一篇精彩而详细的文章。

老式计算社区已经宣布这个月为#MARCHintosh，庆祝所有关于 Mac 的事情。在这里，我们不能满足我们的 Mac 黑客，所以请确保继续发送这些提示。与此同时，请查看我们迄今为止对 Macintosh 的报道，包括这款[全新的 SE/30 逻辑板](https://hackaday.com/2021/03/24/30-year-old-macintosh-se-30-gets-a-brand-new-logic-board/)。

 [https://www.youtube.com/embed/zM_sNItbuhc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zM_sNItbuhc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

