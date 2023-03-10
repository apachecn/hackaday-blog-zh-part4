# 苹果获得 CP/M

> 原文：<https://hackaday.com/2021/05/13/apple-gets-cp-m/>

如果你想在 Mac 上运行 WordStar，[Tom Harte]为 OS/X 提供了[CP/M，看起来会很有趣。当然，运行 Zork 或 Turbo Pascal 可能会更开心，你也可以这样做。](https://github.com/TomHarte/CP-M-for-OS-X)

有很多 Z80 仿真器可以运行 CP/M，但我们发现这个仿真器最有趣的地方是它是用 Objective C 编写的，这是一种在 Mac 和 NeXT 世界中有着悠久历史的语言。

如果你想阅读代码或尝试修改，这个项目是合乎逻辑的。有 BIOS、处理器和 RAM 内存部分。还有一个带有 CP/M BDOS 接口的目录。一旦有了这些，在虚拟 Z80 计算机上启动 CP/M 就相对容易了。

如果你曾经为这个时代的计算机建造过 64K 的内存板，那么看到整个事情减少到大约 50 行代码会有点不安。CPU 在将近 1500 行代码的时候稍微好一点。我们记得在 20 世纪 80 年代研究 BDOS 和 BIOS 接口，这需要阅读汇编语言。如果您今天想学习，C、C++或 Objective C 中有大量易读的例子。

我们已经让 CP/M 在从 [ESP32](https://hackaday.com/2020/08/20/esp32-altair-emulator-gets-split-personality/) 到 [real Z-80](https://hackaday.com/2017/01/02/retrocomputing-for-4-with-a-z80/) 的所有东西上运行。