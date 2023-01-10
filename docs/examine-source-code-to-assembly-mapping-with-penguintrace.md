# 使用 PenguinTrace 检查源代码到程序集的映射

> 原文：<https://hackaday.com/2019/05/09/examine-source-code-to-assembly-mapping-with-penguintrace/>

对于汇编代码之上薄薄的抽象外表下发生的事情没有一个心理模型的 c 程序员注定会遇到麻烦。为了提供一种方便的方式来理解 C 代码被编译成什么以及它是如何在机器上运行的，[Alex Beharrell]创建了 [penguinTrace，一个允许你查看你的代码编译成什么指令，并检查它如何执行的程序](https://penguintrace.org/)。

虽然您可以从标准调试器中获得有些类似的功能，但 penguinTrace 是专门构建的，以便于探索整个过程是如何工作的。您可以单步执行代码编译到的指令，检查变量，并查看堆栈——常见的调试器内容——但其结构更适合探索和学习，而不是完全调试。根据我们学习低级编程时的经验，任何能够帮助新手构建底层正在发生的事情的最重要的心理图景的东西都是好东西。但是，因为它的第二个目的是学习调试器如何工作，所以这也是一个探索这个领域的好机会。

UI 利用 CodeMirror 来提供一个基于浏览器的界面，并可配置为使用 Clang 或 GCC 进行编译。它支持 AMD64/X86-64 和 AArch64 架构，并将在使用 WSL 的 Windows 上运行:如果你有一台运行 Linux、Raspberry Pi 或 Windows box 的 PC，你就可以开始了。代码是 AGPL 授权的，可以在 GitHub 上获得[。因此，如果您想更好地理解编译和运行“hello，world”时会发生什么，请拿一份副本并开始探索。](https://github.com/penguintrace/penguintrace)

不过，这并不是唯一的调试方式——我们之前介绍过[一个允许对 Arduino 平台](https://hackaday.com/2018/11/07/debugging-arduino-is-painful-this-can-help/)进行某种类型调试的应用程序。