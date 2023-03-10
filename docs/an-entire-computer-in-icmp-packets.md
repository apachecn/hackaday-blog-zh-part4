# ICMP 数据包中的整个计算机

> 原文：<https://hackaday.com/2022/01/25/an-entire-computer-in-icmp-packets/>

现代意义上最早的存储程序计算机并不是你可能会想到的 ENIAC 或 Colossus 之类的名字，而是曼彻斯特宝贝(Manchester Baby)，一台 1948 年在曼彻斯特大学建造的实验原型计算机。它的 550 个试管使它具有 20 世纪 40 年代常见的多机架空间填充大小，但它的架构使它成为当今标准下相对简单的处理器。事实上如此简单，以至于[Hrvoje av rak][使用 ICMP 数据包作为其存储，并使用自定义数据包过滤器作为其处理器模拟](https://github.com/hrvach/babyping)来重新创建它。这是一个既优雅又无意义的项目，但正如他所说的，*“这仍然比做毒品或 JavaScript 要好”。*

结果模拟了网络流量转储中婴儿的组合存储和显示管，并给出了一个极好的借口来阅读关于其操作的[。微小的指令集让人想起今天的 RISC 体系结构，但这是虚幻的，因为 1948 年的设计者对时钟周期的关注要少于他们对机器工作的关注。](https://en.wikipedia.org/wiki/Manchester_Baby)

如果早期的计算机引起了你的兴趣，也许值得花点时间去了解一下英国的国家计算机博物馆，然后是 T2 的巨像，原始的电子计算机。

Header: Geni， [CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:Manchester_baby_head_on.JPG) 。