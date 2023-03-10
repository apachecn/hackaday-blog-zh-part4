# 掉进了英特尔微码兔子洞

> 原文：<https://hackaday.com/2022/07/19/down-the-intel-microcode-rabbit-hole/>

名副其实的[chip-red-pill]团队为您提供了一个深入英特尔兔子洞的机会。如果您在 20 世纪 70 年代学习了如何构建 CPU，您将会了解到，例如，您的指令解码器会记录一个寄存器到寄存器的移动，然后点亮一个寄存器以写入公共总线，点亮另一个寄存器以从公共总线读取。如今，事情没那么简单了。除了编译成底层指令集，处理器很少在硬件中编码指令。相反，每条指令都有微码，使正确的事情在正确的时间发生。但是英特尔加密了他们的微码。当然，能加密的也可以[解密](https://github.com/chip-red-pill/MicrocodeDecryptor)。

利用漏洞，可以激活名为红色解锁的未记录调试模式。这允许微码转储，并且解密密钥在里面。该团队为《进攻 22》撰写了一篇关于这种技术的论文，你可以在下面看到一段视频。

到目前为止，双子座湖和阿波罗湖处理器的关键是可用的。这涵盖了相当多的处理器。当然，如果您想尝试类似的利用，还有更多的处理器。

这个团队还做了其他的利用，比如在 Atom CPU 中执行[任意微码。如果你想合作，你可能](https://www.offensivecon.org/speakers/2022/maxim-goryachy.html)[会发现这个有用的](https://hackaday.com/2021/03/26/undocumented-x86-instructions-allow-microcode-access/)。你知道你的 [CPU 有指令瞒着你](https://hackaday.com/2017/07/30/find-instructions-hidden-in-your-cpu/)，不是吗？

 [https://www.youtube.com/embed/V1nJeV0Uq0M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/V1nJeV0Uq0M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

