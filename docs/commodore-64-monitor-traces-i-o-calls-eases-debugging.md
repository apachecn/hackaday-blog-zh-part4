# Commodore 64 监视器跟踪 I/O 调用，简化调试

> 原文：<https://hackaday.com/2022/02/18/commodore-64-monitor-traces-i-o-calls-eases-debugging/>

为 Commodore 64 开发可能是一次有益的逆向计算体验，多亏了[Dave Van Wagner]，他的 [C64 IO_Monitor 项目](https://techwithdave.davevw.com/2021/12/trace-c64-io-kernal-jump-table-calls.html)使事情变得更容易，它打开了记录和跟踪内核 I/O 调用的大门，以便更仔细地检查。顺便说一句，这不是印刷错误。[内核](https://en.wikipedia.org/wiki/KERNAL)负责处理 C64 的底层操作系统例程。有趣的是，正如故事所述，它实际上起源于*内核*的拼写错误，但是这个名字被保留了下来。

[Dave]的程序所做的是跟踪和记录所有通过 Kernal 的输入和输出调用，这包括任何你能想到的函数。像键盘输入、屏幕输出和磁盘或磁带 I/O 这样的东西都被忠实地计数和记录，这使得人们在进行任何类型的开发工作时都可以真正地在较低的级别上进行窥视。考虑到[Dave]喜欢将 Commodore 模拟器移植到各种(有时是不常见的)平台上，这种工具变得非常方便。

有兴趣试试吗？前往该项目的 [GitHub 库](https://github.com/davervw/c64-io_monitor)获取所有必要的文件以及一些使用细节，并享受使调试和开发变得不那么不透明的乐趣。