# 古怪的 X86 指令

> 原文：<https://hackaday.com/2021/02/25/oddball-x86-instructions/>

大卫·莱特曼使十大排行榜闻名遐迩。[Creel]列出了十大最疯狂的 x86 汇编语言指令，这应该会吸引很多黑客读者。你必须承认，汇编语言程序员的比例每年都在下降，所以这不会有很大的吸引力，但如果你对汇编或 CPU 架构感兴趣，这是一种消磨 15 分钟的有趣方式。

有人会说所有的 x86 指令都是疯狂的，尤其是如果你习惯于精简指令集计算机的话。x86 和其他非 RISC 处理器一样，除了厨房水槽之外什么都有。这些指令中的一些可能会帮助您从时间关键的循环中减去最后的 10 纳秒。

还有一些有趣的指令，比如 RDSEED，它可以生成一个真正的随机数。这可能是有用的，但它需要许多时钟周期来运行，并且像任何声称能产生随机数的东西一样，受到许多争议。

不过，我们最喜欢的是 PSHUFB。我们一看到“魔咒先生”就开始了！作为示例输入字符串，我们知道它要去哪里。你可能一辈子都不用这些指令。但是如果你需要他们，现在你会知道的。

如果你真的想学习现代汇编语言，这里有很多帮助。我们偶尔会写一点 [Linux 汇编](https://hackaday.com/2016/06/14/linux-assembly-required/)，只是为了保持练习。

 [https://www.youtube.com/embed/Wz_xJPN7lAY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Wz_xJPN7lAY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

