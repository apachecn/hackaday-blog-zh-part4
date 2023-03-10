# 内部芯片-8

> 原文：<https://hackaday.com/2020/12/07/inside-chip-8/>

某些旧电脑——最常见的是使用 RCA 1802 的电脑——喜欢使用早期形式的字节码解释程序，尤其是游戏。解释器 CHIP-8 创建起来非常简单，但提供的高级功能用本地汇编语言重新创建起来很繁琐。因为有相当数量的简单游戏是用 CHIP-8 编写的，当然也有它的模拟器，所以【River Gillis】决定[看看 CHIP-8 字节码解释器](https://river.codes/emulating-a-computer-part-1/)的内部。

CHIP-8 的部分优势在于它只有 35 条虚拟指令。当你试图把一个游戏和解释器硬塞进一个很小的记忆中时，这是很重要的。请记住，在那个时代，1K 内存并不是一个不寻常的数字，尽管原型芯片 8 主机将有 4K。

虚拟机有 16 个 8 位数据寄存器和一个堆栈。因为这个想法是为了创造游戏，所以有一些功能是有用的。例如，使用 sprites 绘制到屏幕(默认情况下是 64×32 像素的屏幕)，可以自动获得屏幕上任何碰撞的信息。这些指令提供了一些显示和输入设备的虚拟化，通常是十六进制键盘，还提供了将二进制数字转换为二进制编码的十进制数字的能力。

因此，通过设计创建解释器并不困难。然而，[River]必须模拟一台目标机器，这就是第二部分要做的。然而，如果你对逆向计算、逆向游戏感兴趣，或者你只是想更好地理解字节码解释器是如何工作的，这是一本有趣的读物，有很多代码示例。

当您试图节省内存空间并使开发更容易时，定制虚拟计算机实际上并不是一个坏主意。Java 在类固醇上使用了同样的想法，尽管主要是出于不同的原因。P-Code 是另一个类似的系统，其核心是相同的基本概念。

今天，将 CHIP-8 放在一台小型计算机上，使[成为一台超级复古游戏机](https://hackaday.com/2020/06/09/run-your-favorite-8-bit-games-on-an-esp32/)会很有趣。或者买一个旧的 1802 CPU——它们仍然可用。你也可以[制作自己的](https://hackaday.com/2020/01/23/cosmac-elf-lives-again-in-fpga/)。

图片来源:RCA Cosmac VIP BY[Dave Ruske][CC BY 2.0](https://creativecommons.org/licenses/by/2.0/)