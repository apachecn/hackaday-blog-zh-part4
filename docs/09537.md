# 苹果芯片上的 Linux 任重道远

> 原文：<https://hackaday.com/2021/03/21/the-long-journey-ahead-for-linux-on-apple-silicon/>

一个来自 Linux 社区的关于它在计算领域的流行的老笑话讽刺道，Linux 可以在任何东西上运行，包括一些动物。虽然这个笑话有点过时，但 Linux 确实可以在任何计算平台上运行，只需要付出一定的努力。目前的例外是新的苹果 M1 芯片，尽管一个名为 Asahi Linux 的小组正在努力让 Linux 在这种新的硬件上运行。

虽然苹果 M1 是专门为运行 macOS 而设计的，但是一旦所有的问题都解决了，没有任何技术上的理由可以解释为什么 Linux 不能在上面运行。上个月的进度报告概述了当前关注的一些领域，特别是关于引导非 Mac 内核。新的苹果芯片[运行在 ARM 处理器](https://hackaday.com/2020/08/12/degrees-of-freedom-booting-arm-processors/)上，正因为如此，它的功能更像一个嵌入式设备，而不是带有标准化 BIOS 或 UEFI 的 PC。这意味着必须创建许多专有引导过程的变通方法来引导 Linux 内核。幸运的是，已经有在 ARM 上运行的 Linux 版本，所以已经做了很多工作，但是还有很多工作要做。

虽然如果你需要在你自己的个人机器上安装 Linux，目前最好购买一台 x86 机器，但在 M1 芯片上克服 Linux 的所有障碍似乎只是时间问题。如果 Linux 能够利用这些芯片的一些效率和性能优势，它可能会改变 Linux 世界的游戏规则，至少给我们所有人提供了另一种硬件选择。当然，我们仍然需要能够在 ARM 上运行的[软件。](https://hackaday.com/2021/01/22/porting-firefox-to-apple-silicon-tales-from-the-trenches/)

感谢[Mark]的提示！