# 一个很小的 RISC-V 仿真器在没有 MMU 的情况下运行 Linux。是的，它运行厄运！

> 原文：<https://hackaday.com/2022/12/07/a-tiny-risc-v-emulator-runs-linux-with-no-mmu-and-yes-it-runs-doom/>

要运行 Linux，你的计算机必须包括一个硬件内存管理单元，或 MMU，这是一个信条。从某种程度上说，这是真的，因为基于 Linux 的系统要发光，它必须有那个硬件，但事实上，现在对无 MMU Linux 的支持已经有很多年了。多产的黑客【cnlohr】创造了[一个没有 MMU](https://github.com/cnlohr/mini-rv32ima) 的仿真简单 RISCV 处理器，它不仅运行 Linux、[还运行*DOOM*。](https://www.youtube.com/watch?v=YT5vB3UqU_E)

休息时间下面的视频对编写和调试仿真器进行了深入的探讨，更不用说 *DOOM* 的内部工作原理了，但是如果它不是你的东西，就不用担心了。任何东西都可以在 GitHub 库中找到，如果您想亲自尝试，还有简单的说明。

所有这些都是有趣的东西，但当被视为正在进行的针对低端 RISC-V 微控制器的无 MMU Linux 项目链的一部分时，它变得更加有趣。想象一下在相对便宜的 CPU 上运行 Linux 的前景，你就会明白为什么这是一个有趣的前景。即使这不是没有 MMU 运行 Linux 的最意想不到的方式。

 [https://www.youtube.com/embed/YT5vB3UqU_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YT5vB3UqU_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/uZMNK17VCMU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uZMNK17VCMU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

