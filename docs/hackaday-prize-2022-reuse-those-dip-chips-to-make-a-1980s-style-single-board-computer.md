# 2022 年黑客日奖:重新利用这些 DIP 芯片制造一台 20 世纪 80 年代风格的单板电脑

> 原文：<https://hackaday.com/2022/05/28/hackaday-prize-2022-reuse-those-dip-chips-to-make-a-1980s-style-single-board-computer/>

由于严重的芯片短缺仍在拖延新组件的交付，现在可能是一个好时机来看看你的实验室，检查那些你认为“有一天可能会派上用场”的芯片。你可能会发现一个 74xx 系列逻辑的好堆栈，曾经无处不在，但由于强大的微控制器和 FPGAs，今天大部分已经过时。让它们被浪费掉是一种耻辱，所以为什么不用它们来制造一台整洁的 80 年代风格的电脑呢？

带着这个想法，[Anders Nielsen]设计了 [ABN6502:一款基于古老的 6502 处理器](https://hackaday.io/project/184725-abn6502-sbc-r1)的单板计算机，但具有相对现代的接口，如 VGA 监视器输出、PS/2 键盘连接器，甚至无线模块，以简化从 PC 上传固件。一个设计要求是尽量减少所需新部件的数量；对构建 ABN6502 感兴趣的普通黑客可能会将许多芯片放在他们工作室的某个地方。

组件列表看起来像是基于 6502 的计算机的典型物料清单，但具有很大的灵活性，允许部件替换。对于 CPU，支持经典的 NMOS 6502 和基于现代 CMOS 的 65C02，以及提供 I/O 端口和定时器的 6522 配套芯片。一个 ROM 插座既可以容纳现代的快速闪存芯片，也可以容纳传统的但速度较慢的 UV 可擦除 EPROMs。

安德斯没有使用具有复杂刷新要求的 DRAM 芯片，而是使用 32 KB 的 SRAM 来实现主存储器；80 年代买不起，但今天很容易买到。标准的 74xx 系列逻辑芯片将所有组件粘合在一起，同样也有几个选项可以根据用户的喜好添加或删除功能。引脚接头引出 I/O 端口，便于连接外部外设。

ABN6502 的软件库目前仅限于引导加载程序，但基于 CC65 编译器的完整开发工具链应该可以轻松地在该平台上开发各种程序。我们已经展示了[智能无线 ROM 闪存系统](https://hackaday.com/2022/04/05/wireless-bootloader-saves-you-from-swapping-rom-chips/)，以及[6502 驱动 RGB LEDs 的演示](https://hackaday.com/2021/12/23/ws2182s-on-a-6502/)。

 [https://www.youtube.com/embed/w5cA64xof2I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w5cA64xof2I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[hack adayprize 2022](https://prize.supplyframe.com)主办单位:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)