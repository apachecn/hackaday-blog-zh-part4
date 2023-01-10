# 施乐在你附近的桌面上启动

> 原文：<https://hackaday.com/2019/01/22/the-xerox-star-on-a-desktop-near-you/>

那是 1980 年左右，你看到有人在键盘上打字。显示器是图形化的，他们用鼠标完成一份文件，通过网络把它发送到另一台类似的计算机上，在那里另一个用户编辑一下，然后用激光打印机打印出来。考虑到时间框架，你可能会认为这是一台 Mac 电脑，但你错了。施乐之星拥有苹果在麦金塔问世前三年左右“发明”的所有功能。如果你从未听说过这位明星，这并不奇怪。每张售价 1.65 万美元，只卖出了约 2.5 万张。你现在找到一个工作的机会很小，但多亏了[Josh Dersch] [创造的仿真，你今天就可以在你的硬件上试用 Star。如果你想预览一下，可以看看下面这段 1982 年的视频。](https://engblg.livingcomputers.org/index.php/2019/01/19/introducing-darkstar-a-xerox-star-emulator/)

这台机器的结构出奇的复杂。主 CPU 是一台带有多个寄存器的微代码计算机，它运行一种微代码程序，根据运行的内容执行不同的指令集。此外，英特尔 8085 加载了正确的微码，并为键盘、鼠标、软盘和串行端口提供服务。

在实施过程中有一些障碍。首先，ALU 为标志产生标志输出，即使它们没有意义。[Joel]决定在这些时候忽略标志，因为他不希望任何程序依赖于 AND 运算的进位输出。然而，他不得不实现 OR 情况，因为一些软件预期的行为。

另一个问题在于 CPU 的速度和数据路径。有些操作不够快，无法在一个时钟周期内完成。他们中的一些人返回了垃圾，另一些人部分正确。[Joel]认为没有一个健全的程序会依赖于不正确的部分，他似乎是对的。

我们建议你在开始使用这个软件之前阅读一下[Josh 的]帖子，因为这是一篇关于所有部分是如何组合在一起的精彩文章。然而，当你准备好了，你就可以去 GitHub 了。不过这只是基本情况，要做任何有用的事情，你需要一个来自 [Bitsavers](http://bitsavers.org/bits/Xerox/8010/8010_hd_images.zip) 的硬盘镜像。

尽管市场宣传与此相反，大多数现代桌面环境起源于施乐 PARC 公司，建立在 Douglas Englebart 的工作基础上。明星是[仅仅是开启桌面时代](https://hackaday.com/2016/06/26/restoring-the-groundbreaking-xerox-alto/)的机器之一。

 [https://www.youtube.com/embed/wOAm7EiFNu8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wOAm7EiFNu8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

