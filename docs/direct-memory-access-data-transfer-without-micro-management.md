# 直接内存访问:无需微管理的数据传输

> 原文：<https://hackaday.com/2021/03/31/direct-memory-access-data-transfer-without-micro-management/>

在最简单的计算机系统结构中，所有的控制都由 CPU(中央处理器)来完成。这不仅意味着执行影响 CPU 内部寄存器或缓存状态的命令，还意味着将任何字节从内存传输到设备，如存储器和串行、USB 或以太网端口等接口。这种方法被称为“编程输入/输出”，或 [PIO](https://en.wikipedia.org/wiki/Programmed_input%E2%80%93output) ，并在 20 世纪 90 年代初广泛用于例如 [PATA](https://en.wikipedia.org/wiki/Parallel_ATA) 存储设备，包括 ATA-1、ATA-2 和 CompactFlash。

显然，如果 CPU 必须处理每个内存传输，这将开始严重影响系统性能。对于每个内存传输请求，CPU 必须中断正在进行的其他工作，设置并执行传输，并在继续之前恢复其先前的状态。随着存储和外部接口的速度越来越快，这变得越来越不可接受。PIO 不会占用 CPU 周期的百分之几，一个大的传输会占用大部分周期，使系统陷入停顿，直到传输完成。

DMA(直接内存访问)将 CPU 从这些琐碎的任务中解放出来。有了 DMA，外围设备不必要求 CPU 为它们取一些数据，而是可以自己取。不幸的是，这意味着多个系统争夺同一个内存池的内容，这可能会导致问题。因此，让我们看看 DMA 是如何工作的，着眼于弄清楚它如何为我们工作。


## 硬件内存

DMA 的核心是 DMA 控制器:它唯一的功能是在 I/O 设备和内存之间建立数据传输。本质上，它的功能类似于我们都知道并喜欢的 c 语言中的 [memcpy](http://www.cplusplus.com/reference/cstring/memcpy/) 函数。这个函数有三个参数:目的地、源以及从源到目的地要复制多少字节。

[![](img/bc8f85f48150079e11da0f6017587052.png)](https://hackaday.com/wp-content/uploads/2021/02/intel_8237_dma_controller_system_interface-rethemed.png) 以[英特尔 8237](https://en.wikipedia.org/wiki/Intel_8237) 为例:这是来自英特尔 [MCS 85](https://en.wikipedia.org/wiki/Intel_8085#MCS-85_family) 微处理器家族的 DMA 控制器。它具有四个 DMA 通道(DREQ0 至 DREQ3 ),曾在 IBM PC 和 PC XT 中广泛使用。通过链接多个 8237 集成电路，可以增加 DMA 通道的数量，如 IBM PC AT 系统结构中的情况。 [8237 数据表](https://web.cecs.pdx.edu/~mpj/llp/references/Intel-8237-dma.pdf)显示了 8080 级系统中基本(单个)8237 IC 集成的情况:

在一个简单的请求中，DMA 控制器通过拉高 HRQ 来请求 CPU 放弃对系统总线(地址、数据和控制)的控制。一旦授权，CPU 将在 HLDA 引脚上做出响应，此时未完成的 DMA 请求(通过 DREQx 输入)将被处理。DMA 控制器确保在保持总线一个周期后，CPU 每隔一个周期使用总线，以免总线因潜在的长时间运行请求而拥塞。

8237 DMA 控制器支持单字节传输和块传输。按需模式也允许连续转移。这允许在总线上的 PC/PC 上进行 DMA 传输(“ISA”)。

[![](img/9c121a32ed54cecdef64e5aaf80c2cb5.png)](https://hackaday.com/wp-content/uploads/2021/02/stm32f7_system_blocks_diagram-themed.png) 快进几十年，基于 Cortex-M 的 STM32 F7 系列微控制器中的 DMA 控制器既非常相似，也非常不同。该 MCU 不仅有一个 DMA 控制器，还有两个(DMA1、DMA2)，每个都连接到内部系统总线，如 STM32F7 参考手册(RM0385)所述。

在这个 DMA 控制器中，引入了流的概念，其中八个流中的每一个都支持八个通道。这允许多个设备连接到每个 DMA 控制器。在该系统实现中，只有 DMA2 可以执行存储器到存储器的传输，因为只有它通过其两个 AHB 接口连接到存储器(通过总线矩阵)。

与 Intel 8237 DMA 控制器一样，每个通道都连接到一个特定的 I/O 设备，使其能够设置 DMA 请求。这通常是通过向相关设备发送指令来实现的，例如设置寄存器中的位，或者使用更高级别的接口，或者作为设备或外设协议的一部分。然而，在一个流中，在任何给定时间只有一个通道是活动的。

[![](img/798e13cb21b9e5145515b229fdd7d40d.png)](https://hackaday.com/wp-content/uploads/2021/02/stm32f7_dma_controller_diagram-themed.png) 然而，与更基本的 8237 不同，这种类型的 DMA 控制器还可以使用 FIFO 缓冲器来实现诸如改变传输宽度(字节、字等)的功能。)如果这在源和目的地之间不同。

当一个系统中有多个 DMA 控制器时，某种优先级系统总是确保有一个逻辑顺序。对于通道，通道号决定优先级(如 8237)，或者可以在 DMA 控制器的寄存器中设置(如 STM32F7)。多个 DMA 控制器可以放在一个层次结构中，以确保有序。对于 8237，这是通过让级联的 8237 各自使用主控制器上的 DREQx 和 DACKx 引脚来实现的。

## 窥探公共汽车

[![](img/037076f521e5d8b75741eb314c80e99e.png)](https://hackaday.com/wp-content/uploads/2021/02/Cache_Coherency_Generic-themed.png)

Keeping cache data synchronized is essential.

到目前为止，这一切似乎都相当简单明了:只需将 DMA 请求交给 DMA 控制器，让它施展魔法，而 CPU 则去做一些比复制字节更有效率的事情。不幸的是，这里有一个大问题，就是[缓存一致性](https://en.wikipedia.org/wiki/Cache_coherence)。

随着 CPU 获得了越来越多的用于指令和数据的[高速缓存](https://en.wikipedia.org/wiki/Cache_(computing))，从基本的一级(l 1)高速缓存到最近的 L2、L3 甚至 L4 高速缓存，保持这些高速缓存中的数据与主存储器中的数据同步已经成为一项重要功能。

在单核、单处理器系统中，这似乎很容易:从系统 RAM 中获取数据，将它保存在缓存中，一旦系统 RAM 中该点的下一个极其缓慢的访问周期再次打开，就将它写回系统 RAM。为 CPU 添加第二个内核，拥有自己的 L1，可能还有 L2 缓存，突然之间，您必须保持这两个缓存同步，以免任何多线程软件开始返回一些真正有趣的结果。

现在，将 DMA 添加到这种混合物中，您会发现不仅缓存中的数据会发生变化，系统 RAM 中的数据也会发生变化，而所有这些都不会被 CPU 察觉。为了防止 CPU 使用缓存中的过期数据，而不是使用 RAM 或相邻缓存中的更新数据，引入了一个名为[总线窥探](https://en.wikipedia.org/wiki/Bus_snooping)的功能。

这实际上是跟踪缓存中的内存地址，同时监控对 RAM 或 CPU 缓存的任何写请求，并更新所有副本或将这些副本标记为无效。根据具体的系统架构，这可以完全用硬件或硬件和软件的组合来完成。

## 仅仅是开始

在这一点上应该清楚的是，每个 DMA 实现都是不同的，这取决于它被设计用于的系统和它试图满足的需求。虽然 IBM PC 的 DMA 控制器和基于 ARM 的 MCU 中的 DMA 控制器在基本设计上非常相似，并且在总功能集方面没有太大的差异，但在今天的台式计算机和服务器系统中可以找到的 DMA 控制器完全是另一回事。

服务器系统中的 DMA 控制器被迫应对 40 Gbit 和更快的以太网链路、无数通道的基于 PCIe 4.0 的快速 NVMe 存储等等，而不是处理 100 Mbit 以太网连接或 USB 2.0 Fast Speed 的 12 Mbit。如果可能的话，这些都不会过多地困扰 CPU。

在桌面领域，对更高性能的持续推动，特别是在游戏领域，以存储到设备请求的形式，在 DMA 中引发了一个有趣的新篇章，例如英伟达的 [RTX IO 技术](https://www.techspot.com/news/86601-nvidia-rtx-io-technology-promises-faster-load-times.html)。RTX IO 本身基于微软的 [DirectStorage API](https://www.techspot.com/article/2137-next-gen-directx-12/) 。RTX IO 所做的是允许 GPU 处理尽可能多的存储和解压缩资产的通信请求，而不涉及 CPU。这样就省去了将数据从存储器复制到系统 RAM 中，用 CPU 解压缩，然后再次将数据写入 GPU 的 RAM 中的步骤。

## DMA 的攻击

当然，任何好的和有用的特性都必须有一些折衷，对于 DMA 来说，这通常可以在像 [DMA 攻击](https://en.wikipedia.org/wiki/DMA_attack)这样的事情中找到。这些方法利用了这样一个事实，即 DMA 能够直接写入系统内存，从而绕过了许多安全措施。操作系统通常会防止访问内存空间的敏感部分，但 DMA 绕过了操作系统，使这种保护变得无用。

好消息是，为了利用 DMA 攻击，攻击者必须获得对使用 DMA 的设备上的 I/O 端口的物理访问权。坏消息是，如果不损害使 DMA 成为现代计算机的一个重要特征的东西，任何缓解都不可能有任何真正的影响。

虽然 USB(不像 FireWire)本身不使用 DMA，但 USB-C 连接器(带雷电 3/USB 4)增加了 PCIe 通道意味着通过 USB-C 端口的 DMA 攻击可能[成为现实](http://blog.frizk.net/2016/10/dma-attacking-over-usb-c-and.html)。

## 包扎

正如我们在过去几十年中所看到的，对于某些任务来说，拥有专用硬件是非常理想的。我们这些不得不忍受家用计算机的痛苦的人，这些家用计算机不得不放弃对屏幕的渲染，同时花费所有的 CPU 周期从软盘或类似的地方获取数据，他们肯定已经学会享受一个充满 DMA 的世界和专用的协处理器给我们带来的好处。

即便如此，使用 DMA 也存在一定的安全风险。它们的影响程度取决于应用、环境和缓解措施。就像不起眼的`memcpy()`函数一样，DMA 是一个非常强大的工具，可以用来做好事，也可以用来做坏事，这取决于如何使用它。即使我们不得不庆祝它的存在，考虑它在任何新系统中的安全影响也是值得的。