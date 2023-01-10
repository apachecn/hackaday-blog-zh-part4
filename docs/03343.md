# TTL CPU，最大限度地减少其芯片数量

> 原文：<https://hackaday.com/2019/06/23/a-ttl-cpu-minimising-its-chip-count/>

到现在为止，我们应该都已经习惯了由分立逻辑芯片创造出来的种类繁多的 CPU。我们已经看到了从熟悉的冯·诺依曼架构到 RISC 和 74 TTL 衍生物中完成的任何传输触发架构，对于许多对计算机内部工作感兴趣的人来说，新的设计仍然是一个受欢迎的项目。

[Warren Toomey]的 [CSCvon8](https://hackaday.io/project/165950-cscvon8-an-8-bit-ttl-cpu) 是一台有趣的机器，它只用 17 个芯片实现了一台具有 64 位地址空间的 8 位计算机，并且没有诉诸任何涉及微控制器的技巧。它使用 TTL 实现了一个相当传统的冯诺依曼架构，并使用了一些使用现代芯片的技巧，但在几十年前也可以用同样的方式完成。指令微代码存储在 EEPROM 中，ALU 在非常大的 EPROM 中实现，这可能曾经非常昂贵。特别是，在缺少经典 74181 单芯片器件的情况下，总计数中去除了许多分立 TTL 芯片。为了使它有用，RAM 和 EEPROM 各有 32k，还有一个 UART 用于串行访问。整个集成在一个整洁的 PCB 上，并且有一堆演示代码可以开始使用。一切都可以在项目的 GitHub 库中找到[。](https://github.com/DoctorWkt/CSCvon8)

在本文的开始，我们提到了几个非常规的 TTL CPUs。传送触发了我们在 2017 年精选的一个，RISC 的那个是[在这里出现过不止一次的 Gigatron](https://hackaday.com/2019/03/25/how-the-gigatron-ttl-microcomputer-works/) 。