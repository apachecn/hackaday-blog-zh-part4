# 与德州仪器的计算器交谈

> 原文：<https://hackaday.com/2022/03/17/talking-to-a-texas-instruments-calculator/>

德州仪器是一家世界级的半导体公司，但不幸的是，由于根深蒂固的标准化测试，他们在公众中最出名的是过时的消费级计算器。事实上，这些测试标准是如此根深蒂固，以至于自 90 年代初以来，德州仪器就没有更新过这些计算器的硬件。他们仍然在 Z80 微控制器上运行他们的代码，但[Ben Heck]发现自己拥有一个[，其中有一个现代的 ARM 协处理器，因此可以运行 Python](https://www.youtube.com/watch?v=DXvJ8duZqdA) 。

虽然他不确定计算器运行的是 Python 的哪个实现，但他确实把它拆开了，试图尽可能多地弄清楚这台机器在做什么。最明显的区别是 ARM 协处理器，这是其他图形计算器所没有的。在对测试点进行了一些调查后，[Ben]发现 Z80 和 ARM 芯片使用一种非常“简单”的接口通过双串行线相互通信。抛开简洁性不谈，最终[Ben]能够在计算器旁边连接一个端口，让他可以在计算机处于 Python 编程模式时，用计算机向设备发送 Python 命令。

虽然 20 世纪 80 年代计算器运行 Python 程序的用例可能有限，但我们至少可以称赞 TI 在其自建的标准化测试监狱中尝试现代化。也许这是一个起点，让其他人也能找到更有用的东西，让这些机器在课堂之外也能工作。例如，我们已经看到一些 TI-84 被改装成可以连接互联网。

感谢[niksa]的提示！

 [https://www.youtube.com/embed/DXvJ8duZqdA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DXvJ8duZqdA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

