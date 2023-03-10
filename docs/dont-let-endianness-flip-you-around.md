# 不要让端序左右你

> 原文：<https://hackaday.com/2020/08/04/dont-let-endianness-flip-you-around/>

我们今天接触到的大多数处理器架构都是小端系统，这意味着它们以最低有效字节(LSB)的顺序存储和寻址字节。与过去不同的是，当大端体系结构(包括 Motorola 68000 和 PowerPC)更加普遍时，人们通常可以假设从文件中读取的所有二进制数据以及通过通信协议读取的所有二进制数据都是以小端顺序排列的。这通常会工作得很好。

例如，问题来自于使用大端格式的整数的图像格式，包括 TIFF 和 PNG。当以所谓的“网络顺序”直接处理协议时，也要处理大端数据。试图在小端系统上逐字使用这些格式和协议数据显然是行不通的。

幸运的是，交换我们处理的任何数据的字节顺序是非常容易的。

## 维持秩序

如果位可以以任何一种顺序打包，那么在前面用标记来标记数据是有意义的。例如，在 [TIFF](https://en.wikipedia.org/wiki/TIFF) (标记图像文件格式)图像中，文件的前两个字节指示字节顺序:如果他们读取‘II’(来自‘英特尔’)，则文件是小端(le)格式，如果他们读取‘MM’(来自‘摩托罗拉’)，则数据是大端(BE)格式。由于在 UTF-16 和 UTF-32 的情况下，Unicode 文本也可以是多字节的，因此可以选择在文件开头使用[字节顺序标记](https://en.wikipedia.org/wiki/Byte_order_mark) (BOM)对其字节顺序进行编码。

虽然人们可能会认为需要关注大多数代码中的字符顺序，但有必要提醒一下，今天使用的许多处理器架构实际上不是 LE，而是双端(BiE)，允许它们在 LE 或 BE 模式下运行。这些架构包括 ARM、SPARC、MIPS 及其衍生产品，如 RISC-V、SuperH 和 PowerPC。在这些系统上，我们不能假设它运行在 LE 模式下。更有趣的是，这些架构中的一些允许改变每个进程的字节顺序，而无需重启系统。

## 案例研究:处理字节序

最近，我实现了一个简单的服务发现协议( [NyanSD](https://github.com/MayaPosch/NyanSD) ),它使用二进制协议。为了使它不管主机系统的字节序如何都能工作，我使用了我的另一个项目，名为“[字节缓冲](https://github.com/MayaPosch/ByteBauble)，它包含一些函数来轻松地在字节序之间转换。这个实用程序最初是为[nympmqtt](https://github.com/MayaPosch/NymphMQTT)MQTT 库编写的，也允许它在任何系统上工作。

ByteBauble 的字节序特性的使用相当简单。首先必须创建 ByteBauble 类的一个实例，然后它可以用于编写二进制(NyanSD)消息头:

```

ByteBauble bb;
BBEndianness he = bb.getHostEndian();
std::string msg = "NYANSD";
uint16_t len = 0;
uint8_t type = (uint8_t) NYSD_MESSAGE_TYPE_BROADCAST;

```

定义消息体后，消息的长度(`len`)是消息头中唯一超过一个字节的部分。由于 [NyanSD 协议](https://github.com/MayaPosch/NyanSD/blob/master/doc/NyanSD_overview_and_requirements.md)被定义为小端字节序，我们必须确保它总是以 le 顺序写入字节流:

```

len = bb.toGlobal(len, he);
msg += std::string((char*) &len, 2);

```

默认情况下，全局(目标)字节序在字节缓冲中设置为 little-endian。`toGlobal()`模板方法获取要转换的变量及其当前字节序，这里是主机的字节序。然后可以将结果值附加到消息中，如所示。如果输入字符顺序和输出字符顺序不同，则转换该值，否则不采取任何措施。

从字节流中读取的另一种方式非常类似，字节流的已知字节序与 ByteBauble 的`toHost()`模板方法一起使用，以确保我们获得的是预期值而不是反转值。

## 在字节序之间转换

幸运的是，处理器架构不会简单地让我们停留在这些字符顺序模式上。它们中的大多数还带有方便的硬件特性，以便在 LE 和 BE 之间进行转换时执行所需的字节交换操作，反之亦然。尽管可以根据处理器架构使用所需的汇编调用，但使用编译器内部函数更方便。

这也是 ByteBauble 的字节交换例程的实现方式。目前它的目标是 [GCC](https://gcc.gnu.org/onlinedocs/gcc/Other-Builtins.html) 和 [MSVC](https://docs.microsoft.com/en-us/cpp/c-runtime-library/reference/byteswap-uint64-byteswap-ulong-byteswap-ushort?view=vs-2019) 内部函数。对于 GCC，基本过程如下:

```

std::size_t bytesize = sizeof(in);
if (bytesize == 2) {
	return __builtin_bswap16(in);
}
else if (bytesize == 4) {
	return __builtin_bswap32(in);
}
else if (bytesize == 8) {
	return __builtin_bswap64(in);
}

```

正如我们在上面的代码中看到的，第一步是确定我们要处理多少字节，然后调用适当的内部函数。编译器内部的实现取决于目标体系结构在硬件特性方面为该进程提供了什么。最坏的情况是，它可以使用一个原位反向算法在纯软件中实现。

## 确定主机字节顺序

正如我们前面看到的，为了正确地在主机和目标字节序之间转换，我们需要知道前者的字节序是什么，以便知道是否需要任何转换。这里我们遇到了一个问题，很少有现成的操作系统函数，或者我们可以调用它来获取这些信息。

幸运的是，确定主机(或进程)的字节顺序非常容易，如 ByteBauble 所示:

```

uint16_t bytes = 1;
if (*((uint8_t*) &bytes) == 1) {
	std::cout << "Detected Host Little Endian." << std::endl;
	hostEndian = BB_LE;
}
else {
	std::cout << "Detected Host Big Endian." << std::endl;
	hostEndian = BB_BE;
}

```

这个检查背后的想法是一个简单的实验。由于我们需要知道 MSB 和 LSB 在多字节变量中的位置，我们创建了一个新的双字节变量`uint16_t`，将 LSB 的第一位设置为高，然后继续检查第一个字节的值。如果第一个字节的值为 1，我们知道它是 LSB，并且我们正在小端环境中工作。然而，如果第一个字节是 0，我们知道它是 MSB，因此这是一个大端环境。

这种方法的好处在于它不依赖于任何假设，比如检查主机架构，而是直接检查多字节操作发生了什么。

## 包扎

我们可能永远看不到处理这些字节顺序差异的尽头。这既是由于现有文件格式和处理器架构的遗留问题，也是由于某些操作在以大端顺序执行时效率更高的事实(就像网络设备中常见的那些操作)。

幸运的是，正如我们在本文中看到的，处理不同的字节顺序并不复杂。第一步是始终意识到要处理或写入的字节流中的字节顺序。第二步是通过编译器内部函数或包装这些函数的库来有效地使用主机端序。

通过这些简单的步骤，endianness 仅仅是一个轻微的烦恼，而不是一个可以忽略的细节，直到事情着火。