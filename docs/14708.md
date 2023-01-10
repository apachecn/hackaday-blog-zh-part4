# KittyOS:从头开始为 ATmega168 编写一个玩具操作系统

> 原文：<https://hackaday.com/2022/09/05/kittyos-writing-a-toy-os-for-the-atmega168-from-scratch/>

为计算平台编写操作系统是很少有人真正需要做的重要任务之一，无论是为小型微控制器还是大型通用计算机。我们中的许多人花费大量的时间为嵌入式系统开发健壮的代码，当我们陷入一个问题时，偶尔会深入抽象。很多时候，这项工作是在 RTOS 之上，我们认为这是一个已经解决的问题。[Jonathan Diamond]已经获得了一些低级 AVR 黑魔法的知识，以及操作系统内部如何工作的一些细节，因此决定尝试构建一个名为 KittyOS 的玩具操作系统,仅仅是为了学习体验。

[Jonathan]赶紧补充说，这不是一个实用的操作系统，而是一个学习平台，需要添加一些额外的功能才能有用。针对 8 位 AVR ATmega168，它只有 16kB 的闪存和 1kB 的 SRAM，这个小芯片仍然可以很好地运行基本的操作系统——最多四个应用程序任务和一些基本的系统调用支持。

KittyOS 已经支持抢占式多任务处理，具有优先级和对 c 语言编写的应用程序的支持。硬件支持有点有限，只有串行 I/O 和一点 GPIO，但这对演示者来说已经足够了。使用基于 Python 的主机接口，可以将应用程序加载到四个可用插槽中的任何一个，并对每个插槽的运行状态进行控制。这篇文章很长，有很多我们喜欢的关于这些部分的血淋淋的细节，我们很高兴[乔纳森]花时间做了一个适当的报道和一个演示视频，可以在休息后找到。

这些年来，已经有很多这样的 DIY 操作系统出现在这些页面上，比如针对 Arduino Mega/UNO 主板的 [ZARDOS](https://hackaday.com/2021/06/28/tiny-operating-system-for-tiny-computer/) 。变得复杂一点，我们已经看到了 [Snowdrop，它是用纯 x86](https://hackaday.com/2022/06/11/homebrew-an-os-from-scratch-snowdrop-shows-how-its-done/) 编写的，甚至还带有一个基本的解释器。最后，我们应该提到[我们的 RTOS 指南](https://hackaday.com/2021/02/24/real-time-os-basics-picking-the-right-rtos-when-you-need-one/)，以及如何根据您的需求选择最理想的一款。

 [https://www.youtube.com/embed/2dWXGy-ejWM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2dWXGy-ejWM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

