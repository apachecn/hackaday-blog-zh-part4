# 在 ROM 中仿真 6502

> 原文：<https://hackaday.com/2019/07/02/emulating-a-6502-in-rom/>

Gigatron TTL 微型计算机是另类历史的一次实践。如果由于发明和技术的某种奇怪异常，20 世纪 70 年代不是微处理器的时代，那会怎样？如果我们在 70 年代末就已经有了快速、高密度的 ROM 和 RAM，但将微处理器放入硅片的能力超出了我们的理解范围，那会怎样？很明显，我们会想出一种方法来用它进行计算，而 Gigatron 就是答案。这是一台那个时代的电脑，它的中央处理器完全由微码制成。

虽然在怪异的电子设备世界里，Gigatron 是一种受欢迎的产品，但它的创造者[Marcel van Kervinck]却超越了任何人的想象。现在，Gigatron 正在模仿 6502 处理器，这是在 Apple II 和几乎所有其他不运行 Z80 的复古计算机中发现的相同的 CPU。

在 Gigatron 论坛上有一个关于这个的帖子。虽然它仍然处于开发的早期阶段，但 Gigatron 现在可以运行 6502 个机器代码，这样一来，Gigatron 现在是唯一一台没有 CPU 的双核计算机。所有的寻址模式已经实现，连同一半的指令和大部分的状态标志。所有这些都与 Gigatron 现有的视频子系统相互作用，所有代码都可以通过几条指令在 Gigatron 的虚拟 CPU 和 6502 代码之间切换。

这为已经编写的各种各样的软件打开了大门。像 MS Basic 一样，MicroChess 也是可能的。这太好了；Gigatron 最大的缺点是，最初设计时没有现成的代码。当 Gigatron 有了 C 编译器后，这种情况发生了变化，但现在不知何故，我们已经用比 Apple II 少得多的芯片实现了 6502 的逻辑芯片。它并不快(大约是 1 MHz 6502 速度的八分之一)，但在下面的视频中，你可以看到一个咀嚼方块的演示。

 [https://www.youtube.com/embed/9jHlEjr7xJk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9jHlEjr7xJk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

