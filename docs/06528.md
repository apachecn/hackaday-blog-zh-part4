# 赛博 CK 像赛博甲板一样嘎嘎作响

> 原文：<https://hackaday.com/2020/05/15/cyberduck-quacks-like-a-cyberdeck/>

在过去一年左右的时间里，我们看到了 cyberdecks 的流行——那些高度便携、偶尔可穿戴的电脑会让威廉·吉布森感到自豪。我们看到的许多网络平台都是基于 NUCs 或 Raspberry Pi，本质上是后启示录时代的 DIY 笔记本电脑。但是如果你想在旅途中玩微控制器呢？你真的需要传统的计算能力吗？

如果你建立了[kmatch98]的可爱的 cyberd CK，答案是否定的。它有一个文本编辑器，用于以常规方式编写 Python 脚本，还有一个 REPL，用于动态运行命令。

便携式微控制器的最大障碍之一是获得 HID 访问，这样你就可以用键盘进行通信。翻开 cyberd CK，你会发现两个 ItsyBitsy M4——一个用作 USB 主机，另一个控制显示器，并被编程。为了让键盘输入更容易理解，[kmatch98]采用了一个 MicroPython 编辑器来接收来自 UART 的输入。休息时摇摇摆摆地去看雪碧演示，然后留下来看[kmatch98]详细讨论鸭子。

如果你迫不及待想自己做一个，我们能理解。与此同时，你知道吗[你可以直接从手机上编写 CircuitPython 代码？](https://hackaday.com/2019/01/10/code-on-your-phone-with-circuitpython-editor/)

 [https://www.youtube.com/embed/bv5wRY0CV68?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bv5wRY0CV68?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/1XwYP0y4Prg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=2113&wmode=transparent](https://www.youtube.com/embed/1XwYP0y4Prg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=2113&wmode=transparent)

