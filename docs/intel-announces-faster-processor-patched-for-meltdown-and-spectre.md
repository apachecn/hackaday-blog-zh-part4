# 英特尔宣布为 Meltdown 和 Spectre 修补了更快的处理器

> 原文：<https://hackaday.com/2018/12/12/intel-announces-faster-processor-patched-for-meltdown-and-spectre/>

英特尔刚刚[宣布了他们新的 Sunny Cove 架构](https://newsroom.intel.com/articles/new-intel-architectures-technologies-target-expanded-market-opportunities/)，该架构带有许多新的铃铛和哨子。自 2015 年以来，英特尔处理器产品线一直基于 Skylake 架构，因此新的架构对这家全球最大的芯片制造商来说是一股清新的气息。今年，随着硬件漏洞的暴露，他们一直备受关注，[被称为 Spectre 和 Meltdown](https://hackaday.com/2018/01/15/spectre-and-meltdown-how-cache-works/) 。新的设计当然已经针对这些弱点进行了修补。

新架构(据说是 [Ice Lake-U CPU](https://en.wikichip.org/wiki/intel/microarchitectures/ice_lake_(client)) 的一部分)带来了许多新的承诺，如更快的内核、5 个分配单元以及对 L1 和 L2 缓存的升级。还支持 AVX-512 或高级矢量扩展指令集，这将提高神经网络和其他矢量算法的性能。

另一个显著的变化是支持 52 位物理空间和 57 位线性地址支持。今天的 x64 CPUs 只能使用第 0 位到第 47 位来获得 256TB 的地址空间。额外的位意味着 4 PB 的物理内存和 128 PB 的虚拟地址空间。

新产品是在该公司的 10 纳米工艺下演示的，顺便提一下，这与之前推出的 Cannon Lake 相同。新处理器将于 2019 年下半年推出，并被大力宣传为密码学和人工智能行业的福音。据称，对于人工智能来说，内存到 CPU 的距离已经缩短，访问速度更快，并且添加了特殊的加密指令。