# 新零件日:一台 6 美元的 Linux 电脑，你也许可以为它写代码

> 原文：<https://hackaday.com/2018/11/12/new-part-day-a-6-linux-computer-you-might-be-able-to-write-code-for/>

来自廉价电子产品世界的最新消息是运行 Linux 的单板计算机。它值六美元，你现在就可以买到。你甚至可以为它编译代码。

C-Sky Linux 开发板[在淘宝](https://item.taobao.com/item.htm?&id=556322544984)上被列为“OrangePi NanoPi Raspberry Pi Linux 开发板”，尽管有一些公然盗用商标的行为，但这确实是一台运行 Linux 的计算机，售价 7 美元。

该主板基于 NationalChip GX6605S SoC，这是一款独特的芯片，其 ISA 不同于 ARM、x86、RISC-V、MIPS 或其他任何被认为正常的芯片。芯片本身是为机顶盒设计的，但有数量惊人的构建工具[，包括 buildroot、GCC 和对 qemu 的支持](https://github.com/c-sky)。这个芯片背后的公司[正在维护一个内核](https://news.ycombinator.com/item?id=18425643)，对这个芯片的支持已经被[添加到主线内核](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/arch/csky?id=c32e64e852f3f5c0fd709f84bc94736840088375)。是的，不像其他的单板计算机，你可以为这个芯片编译一些东西。

该板的功能包括 64 MB 的 DDR2 RAM、HDMI 输出(带有 1280 x 720 帧缓冲区，最有可能升级到 1080p)，以及运行频率仅为 600 MHz 的 CPU。有几个按钮连接到 GPIO 引脚，两个 USB 主机端口，一个 USB-TTL 端口用于串行控制台，还有几个引脚用于附加 GPIO。似乎没有任何网络，我们也不知道板载存储是什么。

如果你想要一个编译的挑战，这是给你的芯片。