# Z80 上的保护模式！(差不多)

> 原文：<https://hackaday.com/2022/10/23/protected-mode-on-a-z80-almost/>

可能最能实现我们今天认为理所当然的计算体验的微处理器特性是保护模式。具有所需硬件的芯片可以在自己的环境中运行单独的软件进程，从而实现多任务处理和进程间的隔离。旧的 CPU 缺少这个特性，这意味着所有的资源都可以被所有的软件使用。[胡振华] [用 Zilog Z80](https://www.youtube.com/watch?v=DLSUAVPKeYk) 完成了看似不可能的事情，四十多年来首次在芯片上启用了保护模式。他是否发现了一个被其他研究人员遗漏的难以捉摸的未记录的硅片？不完全是，但它是一个聪明的黑客。

Z80 有两个地址空间，一个用于内存，另一个用于 I/O。他将 I/O 请求线通过一个触发器和一些逻辑进行馈送，以便在第一次进行 I/O 调用或执行 rst 指令时调用硬件中断。再加上一小块存储寄存器内容的存储器，他用几个逻辑芯片的成本做了一个带全功能保护模式的 Z80。休息时间下面的视频解释了这一点，我们希望你同意，考虑到手头的资源，这是相当优雅的。对过去的商业 8 位机器来说，这已经太晚了，但看看今天的反计算机设计者如何看待它将会很有趣。

 [https://www.youtube.com/embed/DLSUAVPKeYk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DLSUAVPKeYk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

