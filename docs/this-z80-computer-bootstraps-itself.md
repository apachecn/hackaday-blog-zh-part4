# 这台 Z80 电脑可以自己启动

> 原文：<https://hackaday.com/2020/10/28/this-z80-computer-bootstraps-itself/>

[Plasmode]已经创建了几个 Z80 兼容的电路板设计，其中至少有四个[使用了 oddball Z280](https://hackaday.io/project/175526-zz80mb-a-z280-based-sbc) 。Z280 是 Z80 的一个特殊变体，它可以在没有外部 PROM 的情况下自我引导，这使得它非常适合任何试图在试验板上构建系统的人。根据他的帖子，构建该板的成本约为 35 美元。

虽然 8080 CPU 得到了不少荣耀，但是比 Zilog Z80 好用多了。Z80 只需要一个时钟和一个电源，因此构建系统要容易得多，即使是在试验板上。最重要的是，总线不是多路复用的，它可以自己刷新 DRAM 内存。也许这就是为什么你仍然可以轻松获得 Z80 衍生芯片的原因。不过，有一件事，你需要一个 EPROM 或其他方式来运行一些初始代码来引导你的系统。Zilog 知道这是个问题。在那些日子里，你必须使用一种特殊的工具来刻录 PROM，除非它是可擦除的，并且你有特殊的紫外光来擦除它，否则任何错误都会让你损失一个芯片。

有了 Z280，可以通过引导加载程序加载文件，使设备程序成为自己的 EPROM，就像这个板一样。引导装载程序很简单。它从串行端口加载 256 字节的内存并运行它。该芯片有两种模式，16 位数据总线和 24 位地址。然而，它也可以在 Z80 兼容模式下工作。该芯片有许多创新功能，如内存管理单元和高速缓存，但未能获得成功。

不过，作为一个 CP/M 板，这应该很容易构建。CPU 以 12 MHz 的总线运行，在 RAM 和 EPROM 之间有很酷的兆字节内存。有一个 44 针 IDE 接口和两个 RC2014 扩展连接器。

虽然 35 美元看起来不算多，但使用经典的 Z80，你可以少花很多钱。如果你不介意使用 Arduino 作为支持，你可以花低至 4 美元的[。](https://hackaday.com/2017/01/02/retrocomputing-for-4-with-a-z80/)