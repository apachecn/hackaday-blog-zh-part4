# 家酿只读存储器阅读器保存来自老式小型计算机的数据

> 原文：<https://hackaday.com/2021/08/10/homebrew-rom-reader-saves-data-from-a-vintage-minicomputer/>

你听说过百夫长小型计算机吗？如果没有，不要难过——我们也没有，直到[大卫·洛维特]偶然发现了 1980 年代左右的迷你车的半完整版本，它的所有木材装饰，灰尘包裹的荣耀。除了试图让它再次运行之外，黑客还能做什么呢？

当然，让里根政府的机器运行起来并不是没有风险的，包括可能永远失去机器上的许多 rom 芯片。当发现很难找到一个支持各种芯片的商业只读存储器阅读器时，[【David】决定建造自己的](https://www.youtube.com/watch?v=4pOViNWeeVA)。事实上，他已经成功读取了商业阅读器中的一个芯片，为他提供了一个比较电路的基线，这大大简化了工作。硬件很简单，一个 12 位计数器由三个级联的 74LS161s 构成，用于步进地址，另一个 Arduino Nano 用于提供时钟脉冲并将数据读取到串行端口。

该电路给出了与已知良好读数相同的结果，这意味着结果对其余芯片有效。试验板设置使得支持多个 ROM 引脚变得容易，甚至对于采用-9 伏电压的芯片也是如此。rom 上的数据到底意味着什么，如果有的话，仍然是一个谜，但至少它现在有备份。

在任何人注意到显而易见的事实之前，是的，[大卫]可以使用 555 来记录读者——甚至可能是这个。我们其实很喜欢这样，但是我们明白——有时候你只需要把一个 Arduino 扔在一个工作上，然后完成它。

 [https://www.youtube.com/embed/4pOViNWeeVA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4pOViNWeeVA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

