# 将 C 编译成 PowerPoint

> 原文：<https://hackaday.com/2020/04/06/compiling-c-to-powerpoint/>

如果你在一家大公司工作过，甚至是一家小公司，看起来你花在编写 PowerPoint 图表上的时间比编程的时间还多。【Tom Widenhain 的】视频提问:[我们能把 C 编译成 PowerPoint](https://www.youtube.com/watch?v=LArkm4v5mWA) 吗？观看下面的视频，找出答案。如果您知道[Tom]想要模拟 x86，您会感到惊讶吗？这也让我们感到惊讶，我们不得不注意到视频出现在 4 月 1 日。它看起来确实可行，除了有点笨拙。

这不是图灵机，而是建立了一套聪明的逻辑门。不出所料，[汤姆]是在 Excel 中组装图灵机的家伙。令人惊讶的是，他并不是第一个尝试 C 到 PPT 编译器的人。芝加哥大学在一年前有一个类似的想法，基于汤姆早期的工作，并使用低效的图灵机执行程序。

具有讽刺意味的是， [GitHub](https://github.com/TomWildenhain/pptcc) 上的代码使用 Python 实现了这一壮举，尽管实现并不完整。使用加法器对我们来说不是很明显，所以下面是它的工作原理。当然，首先，你必须处于幻灯片放映模式。加法器的前两行(PowerPoint 文件中的第一张幻灯片)是输入。点击 1 或 0。这填充了中间部分。橙色块是输出，红色块是您必须点击中间部分以填充底部答案的块。有种让我想起[回形针电脑](https://hackaday.com/2015/10/19/diy-computer-1968-style/)的感觉。

因此，虽然这项工作还没有完成，但逻辑门的独创性给我们留下了深刻印象。使用鼠标位置进行数据传输让我们很紧张。正如[Tom]所指出的，尽管如此，我们仍然欢迎您使用他的存储库并继续这个项目。我们不得不承认，比起演示幻灯片，我们更有可能滥用电子表格。

 [https://www.youtube.com/embed/LArkm4v5mWA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LArkm4v5mWA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

