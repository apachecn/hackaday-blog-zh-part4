# Linux 音频的自动调谐

> 原文：<https://hackaday.com/2019/04/10/automated-tuning-of-linux-audio/>

Linux 的音频系统很糟糕。直到你试着建立一个运行 Linux 的录音或广播工作站，你才知道什么是真正的痛苦。二十年前我是这么想的，从那以后什么都没变。当 Linux 被用于服务器空间或一些书呆子的战斗站时，这并不是一个真正的问题，但现在我们有了每个人都使用的小型单板计算机，并希望将其转变为模块化合成器。欢迎来到 paintown，因为 Linux 音频栈很糟糕。

在过去的十年里，[Dynobot]一直致力于改进 Linux 中的音频。这十年来，我一直在阅读 IBM 和 Oracle 的手册，并深入了解如何调整设置以使音频实际工作。所有这些工作现在被合并到一个脚本中，改善了一切。这意味着音频组的优先级被改变，线程优先级更好，延迟更好，对于任何想要建立本地流媒体服务的人来说，网络延迟更好。这不是一切，也没有提到录制多轨音频，但我们将在这里接受婴儿的步骤。

为此有两个相关的 Github 库，第一个包含了针对基于 Debian 的系统的音频调整，包括 Raspberry Pi。这应该可以在任何运行 Debian 的单板计算机上运行，并且已经在所有的 Raspberry Pis、Allo Sparky、ASUS Tinkerboard 和 Odroid C2 上测试过。还有[一个基于 TinyCore 的 Linux 系统版本](https://github.com/dynobot/TinyCore-Sound-Adjustments)，它提高了音频线程的优先级，将线程调度从‘whatever’改为 FIFO，并改善了延迟。如果你正在运行 Linux，并且你正在做一些与音频有关的事情，这就是你所需要的。