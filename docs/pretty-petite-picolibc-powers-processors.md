# 漂亮娇小的 Picolibc 处理器

> 原文：<https://hackaday.com/2022/11/14/pretty-petite-picolibc-powers-processors/>

很多时候，当有人告诉你 X 语言在某方面“更好”时，他们实际上是说它有更好的内置库来完成这项任务。Java 就是一个很好的例子。除了垃圾收集和多重继承之外，这种语言与 C++并没有什么不同，但是标准库非常强大，特别是对于网络。甚至 C 都依赖一个库来提供许多人们认为是语言一部分的函数，例如`printf`。这不是 C 语言的一部分，只是标准库的一部分。当你为一个微型处理器编写程序时，库的选择是至关重要的，[Keith Packard]为你提供了一个选择: [picolibc](https://github.com/picolibc/picolibc) 。

这个库起源于另外两个小型库:Newlib 和 libc 的 AVR 版本。它支持 ARC、ARM、i386、m68k、MIPS、MSP430、Nios II、PPC、RISC-V、Sparc64、x86_64 和 ESP8266/ESP32。

有关于如何将库移植到项目中的文档。这包括一些它期望从操作环境中得到的 API。也有关于库如何使用线程本地存储、锁定和其他技术细节的文档。

比其他选择好吗？这不是我们能说的。你必须在你的确切平台上构建它，并进行自己的比较。然而，它是一个可行的候选，因为它是基于[纽利布](https://hackaday.com/2021/07/19/the-newlib-embedded-c-standard-library-and-how-to-use-it/)的，它应该是相当稳定的。你可以争论该不该用`[printf](https://hackaday.com/2020/07/21/beyond-printf-better-logging-practices-for-faster-debugging/)`。或者你也可以[把身体探进去](https://hackaday.com/2020/06/05/tic-tac-toe-implemented-in-single-call-to-printf/)。但是您也可以使用库的其他部分，而不必深究`printf`。

即使你不需要一个小的库，有时候为你选择的目标通读库代码也是有启发的。例如，你将如何编写一个高效的`strchr`函数？现在，[看看他们是怎么做的](https://github.com/picolibc/picolibc/blob/main/newlib/libc/string/strchr.c)。可移植性在这里是个魔鬼，因为使用一些特定于 CPU 的指令，比如 AVX2 或 SSE，可能会做得更好。

标题图片由[普里西拉·杜·普里兹]提供