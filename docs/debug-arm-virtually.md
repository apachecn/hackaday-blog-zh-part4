# 虚拟调试 ARM

> 原文：<https://hackaday.com/2021/04/23/debug-arm-virtually/>

随着超级强大的桌面计算机的出现，许多开发人员使用某种虚拟或伪虚拟机(VM)。我们在虚拟机中运行 Windows，也在虚拟机中进行内核开发。如果您正在模拟的是同一种类型的计算机，那么过程会更简单，但也可以在 x86 上运行 ARM 代码(反之亦然)，但性能可能比本机运行要慢。QEMU 可能是最著名的程序，它允许 CPU 运行针对不同 CPU 的代码，但默认情况下，它的目标是台式机、笔记本电脑和服务器级机器，而不是微型嵌入式主板。这就是 xPack QEMU Arm 的用武之地。它允许您在主机上的仿真环境中运行和调试嵌入式 Cortex-M 器件。

该工具支持像 Maple 这样的板——这意味着它应该支持 [bluepill](https://hackaday.com/2017/03/30/the-2-32-bit-arduino-with-debugging) ,以及 Nucleo、一些 discovery 板和 Olimex 的几个流行板。他们计划支持 TI、Freescale 和其他公司的几个流行的主板，但没有消息说什么时候会实现。您可以在下面的视频中看到一个来自[EmbeddedCraft]的非常简单的视频示例，即闪烁虚拟 LED，尽管您可能希望在播放音频之前将其静音。

当然也有局限性。例如，你不会得到浮点 M4 指令。据报道，中断处理不是很高保真。您可以将调试消息写入 UART，但是您可以使用半托管来写入主机上的文件描述符。

代码是为 Eclipse 设计的，尽管我们打赌它也能为其他 ide 工作。

 [https://www.youtube.com/embed/Zvbarf1CSGs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Zvbarf1CSGs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

