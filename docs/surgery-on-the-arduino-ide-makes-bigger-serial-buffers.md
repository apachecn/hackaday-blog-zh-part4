# Arduino IDE 上的外科手术产生更大的串行缓冲区

> 原文：<https://hackaday.com/2020/07/13/surgery-on-the-arduino-ide-makes-bigger-serial-buffers/>

众所周知，我并不热衷于 Arduino 基础设施。当然，这些天你有更多的选择，例如 pro IDE 和平台 IO。但是最初的 IDE 总是让我心痛。前几天，当我想做一件非常简单的事情:增加 ATmega32 串行端口上的接收缓冲区时，我意识到有多心痛。我得出的解决方案可能会帮助您做一些其他的事情，所以即使您不需要那个确切的特性，您仍然会发现看到我所做的事情是有用的。

[![](img/210d0343c69b92954df936cf890260fe.png)](https://hackaday.com/wp-content/uploads/2020/06/z80.png) 经历过这些，我真的很纠结。一方面，我鄙视平庸的编辑器，因为它向我隐藏了太多的细节，而且几乎没有提供有用的工具。另一方面，如果你能挖掘出它内部如何工作的细节，我对它的可扩展性印象深刻。

首先，您可能想知道我为什么使用 IDE。简而言之，我不知道。但是当你生产东西给其他人用的时候，你几乎不能忽视它。无论您如何打造自己的个人环境，只要您的代码一进入互联网，就会有人试图在 IDE 中使用它。不久前，我写了一篇由[Just4Fun] 撰写的关于 4 美元 Z80 电脑的文章。我很少有时间做我写的东西，但是我真的很想试试这台小电脑。这些部分组装了一段时间，然后一个 PCB 出来了。我拿到了印刷电路板——你猜对了——它还没组装好。但我终于找到时间完成了它，并启动了 CP/M。

唯一的问题是没有太多好的选择来来回回地将数据传输到个人电脑。看起来最好的办法是做 Intel hex 文件，然后在终端上复制粘贴。我想要更好的，这就把我送进了一个周六早上的兔子洞。我最终得到的是一种在 Arduino IDE 中创建自己的菜单的方法，以便根据项目的目标硬件来设置编译器选项。这是一个值得了解的技巧，因为它将在这个问题之外派上用场。

## 问题:Arduino 串行缓冲区大小限制

我不会用让电路板工作的细节来烦你，因为你只会关心你是否有一个。如果你真的想关注的话，可以在 Hackaday.io 的讨论中找到细节。但结果是，对于 XModem 传输，[Just4Fun]感觉默认的 Arduino 串行缓冲区不够大，不够可靠。它看起来确实适用于默认的 64 字节缓冲区，但是 XModem 发送的数据比这个多，很容易想象它会溢出。

更新缓冲区能有多难？从某一方面来说，这是微不足道的。另一方面，这非常困难，因为工具非常想帮助你。

## 工具链

小计算机项目使用真正的 Z80 芯片，并使用 ATMega32A 用于几乎所有的支持功能。它产生时钟，充当串行端口，充当磁盘驱动器，等等。然而，ATMega32 并不直接支持 Arduino IDE，所以你必须为它安装一个工具链。这个项目需要 MightyCore，所以我用了它。

硬件串行库都是使用#define 语句设置的，允许您调整缓冲区大小。默认情况下，如果您没有进行任何设置，您将获得一个基于处理器提供的 RAM 容量的默认值:

```

#if !defined(SERIAL_TX_BUFFER_SIZE)
#if ((RAMEND - RAMSTART) &lt; 1023)
#define SERIAL_TX_BUFFER_SIZE 16
#else
#define SERIAL_TX_BUFFER_SIZE 64
#endif
#endif
#if !defined(SERIAL_RX_BUFFER_SIZE)
#if ((RAMEND - RAMSTART) &lt; 1023)
#define SERIAL_RX_BUFFER_SIZE 16
#else
#define SERIAL_RX_BUFFER_SIZE 64
#endif
#endif

```

## 做出改变

这很简单，对吧？只需在`HardwareSerial.h`加载之前定义这些符号。啊哦。该文件由`Arduino.h`加载。IDE 希望将它添加到您的程序中，并强制它成为第一个。似乎有一些 IDE 版本会检查你是否已经包含了它，这样它们就不会包含两次，但是 1.8.5 版本似乎没有这样做。也许我可以在首选项中添加一些选项传递给编译器。没有。反正不是通过 IDE。

不是说我没尝试过很多东西。当然，简单地改变核心库是很诱人的。但这很糟糕。您以后可能需要默认值。如果更新工具链，将会丢失更新。我想避免这种情况。网上有人建议做一个平台文件的拷贝，修改一下。还是不理想。

## 使用自定义错误报告测试您的假设

我可以看出我尝试的东西不起作用，因为我会将`#if`语句和`#error`语句暂时放在`HardwareSerial.cpp`中。例如:

```

#if SERIAL_RX_BUFFER_SIZE==256
#error 256
#endif

```

现在，如果编译导致错误 256，我知道我能够设置大小。如果不是，那么系统在抵制我的改变。

## 折衷:在面板级别添加菜单选项

我真的想要一种方法来改变我的项目，并设置串行缓冲区的大小。我失败了。我做的是对 Mighty Core 提供的 boards.txt 做了修改。是的，我将不得不注意覆盖我的更改的升级，但它们很简单，很明显它不见了。

[![](img/4e05818890acbb7f5ea42a56a7027109.png)](https://hackaday.com/wp-content/uploads/2020/06/ide.png)

原因很明显，我为 IDE 创建了一个菜单，只有在使用 ATMega32 for Mighty Core 时才会出现。此菜单允许您选择一些预设的缓冲区大小。

这项工作分为三个部分:

1.  你必须告诉 IDE 你有一个菜单项和它的样子。
2.  新项目需要设置一些编译器选项。
3.  因为现有的系统也设置了一些编译器选项，所以你必须确保不要破坏它们。

第一部分很简单。`boards.txt`文件(对我来说)在`~/.arduino15/packages/MightyCore/hardware/avr/2.0.5/boards.txt`里。靠近顶部有一个菜单键列表，我把我的添加到了末尾:

```

# Menu options
menu.clock=Clock
menu.BOD=BOD
menu.LTO=Compiler LTO
menu.variant=Variant
menu.pinout=Pinout
menu.bootloader=Bootloader
menu.SerialBuf=Serial Port Buffers (RX/TX)

```

接下来，我向下移动文件，将我的菜单添加到 ATMega32 的现有 LTO 菜单选项之前:

```

32.menu.SerialBuf.disabled=Default
32.menu.SerialBuf.disabled.compilerSB.c.extra_flags=
32.menu.SerialBuf.disabled.compilerSB.cpp.extra_flags=

32.menu.SerialBuf.SB64=64/64
32.menu.SerialBuf.SB64.compilerSB.c.extra_flags=-DSERIAL_RX_BUFFER_SIZE=64 -DSERIAL_TX_BUFFER_SIZE=64
32.menu.SerialBuf.SB64.compilerSB.cpp.extra_flags=-DSERIAL_RX_BUFFER_SIZE=64 -DSERIAL_TX_BUFFER_SIZE=64

32.menu.SerialBuf.SB128=128/128
32.menu.SerialBuf.SB128.compilerSB.c.extra_flags=-DSERIAL_RX_BUFFER_SIZE=128 -DSERIAL_TX_BUFFER_SIZE=128
32.menu.SerialBuf.SB128.compilerSB.cpp.extra_flags=-DSERIAL_RX_BUFFER_SIZE=128 -DSERIAL_TX_BUFFER_SIZE=128

32.menu.SerialBuf.SB12864=128/64
32.menu.SerialBuf.SB12864.compilerSB.c.extra_flags=-DSERIAL_RX_BUFFER_SIZE=128 -DSERIAL_TX_BUFFER_SIZE=64
32.menu.SerialBuf.SB12864.compilerSB.cpp.extra_flags=-DSERIAL_RX_BUFFER_SIZE=128 -DSERIAL_TX_BUFFER_SIZE=64

32.menu.SerialBuf.SB256=256/256
32.menu.SerialBuf.SB256.compilerSB.c.extra_flags=-DSERIAL_RX_BUFFER_SIZE=256 -DSERIAL_TX_BUFFER_SIZE=256
32.menu.SerialBuf.SB256.compilerSB.cpp.extra_flags=-DSERIAL_RX_BUFFER_SIZE=256 -DSERIAL_TX_BUFFER_SIZE=256

32.menu.SerialBuf.SB25664=256/64
32.menu.SerialBuf.SB25664.compilerSB.c.extra_flags=-DSERIAL_RX_BUFFER_SIZE=256 -DSERIAL_TX_BUFFER_SIZE=64
32.menu.SerialBuf.SB25664.compilerSB.cpp.extra_flags=-DSERIAL_RX_BUFFER_SIZE=256 -DSERIAL_TX_BUFFER_SIZE=64

32.menu.SerialBuf.SB25632=256/32
32.menu.SerialBuf.SB25632.compilerSB.c.extra_flags=-DSERIAL_RX_BUFFER_SIZE=256 -DSERIAL_TX_BUFFER_SIZE=32
32.menu.SerialBuf.SB25632.compilerSB.cpp.extra_flags=-DSERIAL_RX_BUFFER_SIZE=256 -DSERIAL_TX_BUFFER_SIZE=32

```

## 菜单结构

您可以看到,`32.menu`对象将该处理器的所有项目组合在一起。下一部分是我们的菜单键(`SerialBuf`)。之后是每个内存项目的唯一密钥。重要的是你不要重复使用这些。因此，举例来说，如果你有两把`SB64`钥匙，只有一把可以用。

如果你停在那个键上，加上一个等号，你就可以给这个菜单项分配你想要显示的文本。例如“默认”或“64/64”您还可以使用属性扩展键，如果选项处于活动状态，将会设置该属性。

例如，如果你选择 256/256，那么`compilerSB.c.extra_flags`属性将被设置。顺便说一下，这个名字是我起的，你马上就会明白为什么了。

## 和平共处

没有叫`compilerSB.c.extra_flags`的属性。正确的属性是`compiler.c.extra_flags`。然而，强大的核心`LTO`选项使用相同的密钥。这就是为什么新菜单首先出现并且设置一个假属性很重要。然后`LTO`代码需要稍微修改一下:

```

# Compiler link time optimization
32.menu.LTO.Os=LTO disabled
32.menu.LTO.Os.compiler.c.extra_flags={compilerSB.c.extra_flags}
32.menu.LTO.Os.compiler.c.elf.extra_flags=
32.menu.LTO.Os.compiler.cpp.extra_flags={compilerSB.cpp.extra_flags}
32.menu.LTO.Os.ltoarcmd=avr-ar

32.menu.LTO.Os_flto=LTO enabled
32.menu.LTO.Os_flto.compiler.c.extra_flags={compilerSB.c.extra_flags} -Wextra -flto -g
32.menu.LTO.Os_flto.compiler.c.elf.extra_flags=-w -flto -g
32.menu.LTO.Os_flto.compiler.cpp.extra_flags={compilerSB.cpp.extra_flags} -Wextra -flto -g
32.menu.LTO.Os_flto.ltoarcmd=avr-gcc-ar

```

最大的变化是每组标志都添加到新菜单的自定义属性中。这样，所有的标志都被放入正确的属性`compiler.c.extra_flags`。

我设置了错误陷阱来捕捉所有的情况，以确保它们被设置正确。此外，在移除这些陷阱之后，我可以看到我的内存使用量相应地增加了。

## 定制

当然，如果您想要不同的东西，您可以修改参数。在 Arduino.h 文件接管之前，您也可以使用这个技巧来设置其他参数。有一些关于如何设置平台定义的[文档](https://arduino.github.io/arduino-cli/platform-specification/)，包括`boards.txt`。

对我来说，制作一个包含相同信息的定制`boards.txt`文件可能会更好，但是我需要把 Mighty Core 的其余部分带走。相反，我只保留了一个名为 boards.txt.custom 的文件的副本，如果我的菜单消失了，我只需将该文件与 boards.txt 文件进行比较，看看发生了什么变化。

当然，如果你不必支持人们使用 IDE，也许就放弃吧。 [Pro IDE](https://hackaday.com/2019/10/21/the-arduino-ide-finally-grows-up/) 更好，即使它确实有一些缺点。另外，总有[平台。](https://hackaday.com/2017/04/07/platformio-and-visual-studio-take-over-the-world/)