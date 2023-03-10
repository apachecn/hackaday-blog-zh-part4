# 裸机 STM32:探索内存映射 I/O 和链接器脚本

> 原文：<https://hackaday.com/2020/12/23/bare-metal-stm32-exploring-memory-mapped-i-o-and-linker-scripts/>

在本系列的第一部分中，我们简要介绍了在 STM32 微控制器上运行裸机应用程序所需的步骤。虽然这使我们能够快速获得有趣的东西，但有两个基本元素使 MCU 如此易于使用。一个是在硬件方面，以所谓的内存映射 I/O(输入/输出)的形式，另一个是在我们构建固件映像时传递给链接器的文件中包含的信息。

硬件外设寄存器的存储器映射是处理器内核访问它们的直接方式，因为每个寄存器都可以作为一个存储器地址来访问。这对于编写固件代码和测试都很方便，因为我们可以使用单元或集成测试专用的内存映射。

我们将深入了解这种测试方式，以及这些链接器脚本文件是如何连接到内存布局的。

## 一直以来都是记忆

类似于 UNIX 的“一切都是文件”哲学，对于 Cortex-M MCU，可以说“一切都是内存地址”。将设备映射到平面内存空间实际上是计算机系统的常用方法。甚至英特尔 x86 系统也使用这种方法，在引导时检测 ISA、PCI、SMBus、AGP 和 PCIe 设备，并将其映射到平面寻址空间。

顺便说一句，这个属性还导致了 32 位 x86 系统上的奇怪情况，大约 4 GB 的内存地址空间限制无法支持 4 GB RAM，因为视频卡的 RAM 也将被映射到寻址空间。当 GPU 上的 VRAM 增加到超过 512 MB 时，这就成了问题，所有这些都必须映射到同一个寻址空间。

但是回到微控制器。cortex-M MCU 还有一个 32 位地址空间，从 0x0000 0000 到 0xFFFF FFFF:

[![](img/18103d9320eca92580dc1c16d2df63d1.png)](https://hackaday.com/wp-content/uploads/2020/11/stm32f051_memory_map.png)

STM32F051 memory map from its datasheet.

默认情况下，STM32F0 MCUs 上的闪存从 0x0800 0000 开始，从 0x0000 0000 开始的用于映射到引导介质。默认情况下，这是闪存，但也可以使用 BOOT0/1 配置位切换为映射到外部或内部 RAM:

[![](img/14eeea5c9686a4d3ac8f09b4459680eb.png)](https://hackaday.com/wp-content/uploads/2020/11/stm32f042_rm0091_boot_configuration.png)

Boot mode configuration for STM32F0xx (RM0091, chapter 2.5).

这显示了内存映射是多么灵活:无需更改第一阶段引导加载程序，相同的地址总是可以在引导时加载，引导区的内容很容易切换到不同的源。

## 链接时间到了

在编译后的代码被组装成最终的固件映像之前，链接器工具必须知道如何布置数据以及一些其他细节，比如入口点。这个信息在[链接器脚本](https://wiki.osdev.org/Linker_Scripts)中描述，它使用链接器工具(通常是 ld)理解的语法。让我们以 STM32F042 目标的[链接器脚本为例:](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/linker/stm32f0/stm32f042x6.ld)

* * *

**条目**(复位 _ 处理程序)

这指定了将放入结果二进制文件中作为`.text`(代码)段开始的段(函数)的符号。当 MCU 启动时，这是从闪存启动时执行的第一个代码。这里我们以`Reset_Handler`函数为目标。

* * *

**_ estack**= 0x 20001800；

这将设置堆栈末尾的地址(e stack)。堆栈从 0x2000 0000 (SRAM 开始)开始，向上增长到指定的极限。对于 STM32F042 MCU 上的 6 kB SRAM (0x1800 ),这意味着堆栈可以扩展到整个 SRAM 的大小。显然，这不会给动态分配堆留下任何空间。

* * *

**内存**

这个部分设置了不同的内存区域，以及它们的权限、起始和长度。对于 STM32F042，我们只有两个区域，FLASH(读/执行)和 RAM(读/执行/写)，长度分别为 32K 和 6K 字节。

* * *

**章节**

这定义了各个输出部分的属性。这也决定了各部分在闪存中的结束顺序，对于我们的 MCU 来说，这意味着`.isr_vector`中的向量表和类似的启动代码先出现，然后是`.text`中的固件代码和`.rodata`中的常量。

接下来是初始化数据(`.data`)和未初始化数据(`.bss`)部分以及一些更特殊的部分。最后是`._user_heap_stack`部分，它提供了一些信息，允许链接器检查设备上是否有足够的 RAM 和 FLASH 来存储我们的代码。

然后，当我们将链接时间标志`--print-memory-usage`添加到`ld`时，当对象被组装成最终的 ELF 图像时，我们可以看到类似这样的输出:

```
Memory region         Used Size  Region Size  %age Used
           FLASH:        9956 B        32 KB     30.38%
             RAM:        4008 B         6 KB     65.23%

```

## 内存映射单元测试

到目前为止，我们已经很好地了解了 STM32 MCUs 的存储器架构，以及我们的代码如何适用于它们。任何曾经不得不在 MCU 上编写寄存器级代码的人都可以证明，经历无数次写入-刷新-中断-调整-重新刷新-仍然中断的循环可能会相当令人沮丧，即使有人可以运行一次或十几次调试器来解决问题。

我发现这里有一种方法非常有用，那就是首先用本地测试来测试我的代码，看看我的代码是否正确地写了适当的寄存器。这也允许集成到 CI/CD 系统中，可以运行单元测试，然后自动比较所有寄存器的值。

作为一个例子，考虑我的 [Nodate](https://github.com/MayaPosch/Nodate) 框架中的 [GPIO 外设测试](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/cpp/tests/gpio_test.cpp)。它像在 STM32 固件项目中一样使用 GPIO 类，然后检查 GPIO 外设的寄存器。由于这些测试不能在 STM32 微控制器上运行，很明显，这不是在真实的硬件上使用远程 GDB 魔术。

所有 Nodate 类都包括一个公共头(`common.h`)，它通常包括[设备专用头](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/cpp/core/include/common.h)。相反，在同一个测试文件夹中包含了一个[不同的头文件](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/cpp/tests/common.h)，它定义了 Nodate 代码使用的外围结构和预处理器语句。例如 STM32F0 上的 GPIO 外设:

```

struct GPIO_TypeDef {
  __IO uint32_t MODER;        //!< GPIO port mode register,                     Address offset: 0x00      
  __IO uint32_t OTYPER;       //!< GPIO port output type register,              Address offset: 0x04      
  __IO uint32_t OSPEEDR;      //!< GPIO port output speed register,             Address offset: 0x08      
  __IO uint32_t PUPDR;        //!< GPIO port pull-up/pull-down register,        Address offset: 0x0C      
  __IO uint32_t IDR;          //!< GPIO port input data register,               Address offset: 0x10      
  __IO uint32_t ODR;          //!< GPIO port output data register,              Address offset: 0x14      
  __IO uint32_t BSRR;         //!< GPIO port bit set/reset register,      Address offset: 0x1A 
  __IO uint32_t LCKR;         //!< GPIO port configuration lock register,       Address offset: 0x1C      
  __IO uint32_t AFR[2];       //!< GPIO alternate function low register,  Address offset: 0x20-0x24 
  __IO uint32_t BRR;          //!< GPIO bit reset register,                     Address offset: 0x28      
};

```

在相关的 [`common.cpp`](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/cpp/tests/common.cpp) 源文件中，这种类型的实例在栈上被创建，具有全局可用的指针引用(例如`GPIOA`),如由 ST 提供的设备头中的预处理器语句所发生的那样。当然，它们会将这些外设实例放在 RAM 中的特定偏移量处，以匹配外设寄存器。然而，对于我们的目的来说，这是不相关的，并且大大简化了我们的代码。

```

GPIO_TypeDef tGpioA;
GPIO_TypeDef* GPIOA = &tGpioA;

```

有了这一点，框架的代码将愉快地使用这些全局变量，就好像它们是 MCU 寻址空间的偏移量一样，使我们能够读出我们的 GPIO 寄存器，并查看我们正在测试的代码在每次运行后的表现。

## 定义成功

通常，每个寄存器是一个 32 位字段。验证测试结果的最简单方法是使用 MCU 的参考手册，预先确定我们希望从无符号整数字段读取什么值。一个简单的整数比较将允许我们的验证系统给出“错误”或“正确”的响应。虽然有效，但这也是相当无用的。

虽然“通行证”很好，但它可能会给年轻玩家带来大峡谷般的陷阱，通常被总结为“所有测试都是绿色的，在生产中爆炸”。也就是说，不可能肯定地说一个特定的(单元)测试是完美的，只能说一个问题还没有被发现。这就是手工验证非常有用的地方，尤其是当测试用例变得更大更复杂的时候。

此外，还必须能够打印出哪些测试结果被拒绝，以及哪些输入参数。对于迄今为止我运行的大多数测试，我在终端中使用简单的寄存器值打印输出，然后我可以将它放在参考手册中的寄存器旁边，以便于比较。如上面链接的 GPIO 测试文件所示，这是使用`<bitset>` STL 头完成的:

```

std::cout << "GPIOA" << std::endl;
	std::cout << "MODER:  \t" << std::bitset<32>(GPIOA->MODER) << std::endl;
	std::cout << "PUPDR:  \t" << std::bitset<32>(GPIOA->PUPDR) << std::endl;
	std::cout << "OTYPER: \t" << std::bitset<32>(GPIOA->OTYPER) << std::endl;
	std::cout << "OSPEEDR:\t" << std::bitset<32>(GPIOA->OSPEEDR) << std::endl;
	std::cout << "IDR:    \t" << std::bitset<32>(GPIOA->IDR) << std::endl;
	std::cout << "ODR:    \t" << std::bitset<32>(GPIOA->ODR) << std::endl;

```

这将把`uint32_t`类型转换成一个位域，然后打印如下:

```
GPIOA
MODER:          00000000000000000000000001000000
PUPDR:          00000000000000000000000001000100
OTYPER:         00000000000000000000000000000000
OSPEEDR:        00000000000000000000000000000000
IDR:            00000000000000000000000000000000
ODR:            00000000000000000000000000001000

```

人们可以通过将它分成[个小块](https://en.wikipedia.org/wiki/Nibble)来使阅读起来更加方便，但是这将留给读者作为练习。

## 包扎

本文主要关注 STM32 MCUs 的 STM32F0 系列是有原因的:它们的内存层次结构并不复杂。F4、F7 和 H7 系列的 MCU 具有更复杂的存储器映射。然而，本文中涉及的基础知识仍然适用。

在这一点上，内存映射 I/O 的灵活性以及将其集成到测试和验证系统中的容易程度应该是非常清楚的。如果你对这篇文章中涉及的这个或其他主题有任何建议或意见，欢迎在评论中留下。