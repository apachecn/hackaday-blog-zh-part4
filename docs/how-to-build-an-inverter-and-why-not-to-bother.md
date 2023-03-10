# 如何建立一个逆变器，为什么不麻烦

> 原文：<https://hackaday.com/2018/09/30/how-to-build-an-inverter-and-why-not-to-bother/>

如今，买到便宜的 DC 转交流逆变器简直是轻而易举。它们几乎出现在每一家折扣店或百货店，让你在没有插座的地方神奇地插上电源设备。你的车需要 120 或 240 伏交流电吗？没问题——一个插入打火机插座的小装置只需几美元就可以买到。

那么这些商品值得你自己打造吗？大概不会像[【great Scott！]解释道](https://www.youtube.com/watch?v=zASxHFxf6oY)，但是了解它们如何工作以及它们的局限性可能会对你的设计有所帮助。最便宜和最常见的逆变器具有改进的方波输出，产生的波形对大多数电子设备来说足够好，避免了产生纯正弦输出的额外费用。他解释说，波形只是一个方波，在过零点有轻微的延迟，以实现步进模式，并展示了一个简单的 H 桥电路来产生它。他选择用 Arduino 驱动输出部分，以便轻松产生过零延迟。他用这个低压逆变器来证明，要克服感性负载和输出反馈缺失引起的尖峰，设计需要多复杂。

一句话:知道逆变器是如何工作的很好，但有些东西买比造好。当然，这不会阻止人们建造它们，而且知道你在这个领域所做的事情在过去已经让 T2 赚了大钱。

 [https://www.youtube.com/embed/zASxHFxf6oY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zASxHFxf6oY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

