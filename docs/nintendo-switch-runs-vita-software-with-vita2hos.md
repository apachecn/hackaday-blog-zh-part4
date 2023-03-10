# 任天堂 Switch 用 Vita2hos 运行 Vita 软件

> 原文：<https://hackaday.com/2022/03/06/nintendo-switch-runs-vita-software-with-vita2hos/>

PlayStation Vita 粉丝的好消息——[来自[Sergi "xerpi" Granell]](https://github.com/xerpi/vita2hos) 的一个新项目允许用户在任天堂最新的印钞机 Switch 上运行为索尼以前的手持系统编写的软件。需要说明的是，在 vita2hos 项目能够运行商业游戏(如果有可能的话)之前，还有很长的路要走。但它已经能够在交换机上运行简单的 CPU 渲染的 Vita homebrew 二进制文件，证明这个概念是合理的。

[![](img/0d482e95471290948371f21943732b91.png)](https://hackaday.com/wp-content/uploads/2022/03/switchvita_detail.png)

Running a Vita CHIP-8 emulator on the Switch. Credit: [Modern Vintage Gamer](https://www.youtube.com/watch?v=tLAhhUKsWck)

在技术层面上，vita2hos 与 WINE 并无不同，它使兼容 POSIX 的操作系统(如 Linux、Mac OS 和 BSD)能够运行 Windows 程序，只要它们使用相同的处理器架构。由于交换机的 ARM v8 处理器能够在 32 位兼容模式下运行时执行为 Vita 的 ARM v7 编译的代码，因此没有必要进行仿真。该项目只需要足够快地为运行程序提供类似工作的例程，没人知道。当然，说起来容易做起来难。

根据项目页面，目前最大的障碍是 3D 图形支持。正如你所想象的，许多 Vita 游戏已经将系统的图形硬件推到了极限，这使得捕捉所有小边缘情况变得异常困难，当项目扩展到支持商业游戏时，这些小边缘情况无疑会出现。但是对于自制的 Vita 游戏和实用程序来说，甚至可能不使用系统的 3D 硬件，增加兼容性会容易得多。例如，[已经能够运行【xerpi】自己的 CHIP-8 模拟器](https://github.com/xerpi/VITA-8)。

[xerpi]提供了如何将 vita2hos 和要测试的 vita 可执行文件[安装到已经被入侵的任天堂 Switch](https://hackaday.com/2018/07/01/nintendo-switch-gets-internal-trinket-hardmod/) 上的说明，如果你想试试的话。但是，除非你有开发 Vita 或 Switch 的经验，并且愿意伸出援手，否则你可能希望等到事情稍微成熟一点的时候再做这件事。

感谢[NeoTechni]的提示。