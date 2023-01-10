# 西部数据向世界发布他们的 RISC-V 内核

> 原文：<https://hackaday.com/2019/02/13/western-digital-releases-their-risc-v-cores-to-the-world/>

一个大学研究项目的成果终于变成了真正的硅。RISC-V，完全开放的 ISA，正在开发板、类似 Arduino 的东西和一些轻型物联网的东西中取得进展。这很好，但在你能在实际产品中找到 RISC-V 内核之前，这没有任何意义。在这方面，RISC-V 的最大希望看起来是存储制造商 Western Digital。他们将把 RISC-V 放在他们所有的驱动器中，并且他们刚刚发布了他们自己的核心版本，SweRV 。

去年，Western Digital 惊人地宣称[他们将把硅的消耗](https://www.westerndigital.com/company/newsroom/press-releases/2017/2017-11-28-western-digital-to-accelerate-the-future-of-next-generation-computing-architectures-for-big-data-and-fast-data-environments)转移到 RISC-V 上，每年向市场投放 10 亿个 RISC-V 内核。这是一个巨大的消息，类似于苹果公司说他们不会再打扰 ARM 了。当然，这些核心不一定是面向用户的，但至少我们有所收获。

就 Western Digital SweRV 内核的技术规格而言，它是一个 32 位有序内核，目标实现工艺为 28 纳米，运行频率为 1.8GHz。每 MHz 的性能很好，如果你想要一个芯片或设备来与 SweRV 内核进行比较(这是一个不精确的比较，因为我们在这里只是谈论一个*内核*而不是整个 CPU 或设备)，我们正在寻找一个介于十年前的 iPhone 或非常早期版本的 Raspberry Pi 和现代平板电脑之间的东西。同样，这是一个不精确的比较，但在这一点上不能进行直接的比较。

由于 Western Digital 将 SweRV 内核的整个设计放在了 Github 上，您也可以下载并模拟内核。现在它只是稍微有点没用，但是这个设计已经在 Verilator 中得到验证；在便宜的现成 FPGA 开发板上运行这个几乎是徒劳的。然而，这确实意味着在将 RISC-V 带到大众中，以及每年在 10 亿个设备中放置开放内核方面取得了进展。