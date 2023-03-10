# 一次编写，随处运行:正确的跨平台编程

> 原文：<https://hackaday.com/2020/03/04/write-once-run-everywhere-cross-platform-programming-done-right/>

早在 20 世纪 50 年代，编程语言的目标之一就是创造一种以抽象、高级的方式编写汇编语言概念的方法。这将允许相同的代码在那个时代和随后的几十年中广泛不同的系统架构中使用，只需要一个翻译单元(编译器)将源代码转换为目标架构的机器指令。

其他语言，如 BASIC，会使用提供底层硬件更抽象视图的运行时，但代价是大量的性能。虽然 8 位家用计算机的时代已经过去很久了，但是跨平台开发的话题在今天仍然是高度相关的，无论是谈论桌面、嵌入式还是服务器开发。或者全部同时发生。

今天我们来看看跨平台的景观，好吗？

## 定义可移植代码

可移植代码的基本定义是不受特定硬件平台或平台子集约束或限制的代码。这意味着不应该有针对特定硬件地址或寄存器的代码，或者假设硬件的特定行为的代码。如果不可避免地要使用这些参数，这些参数将作为外部配置数据提供给每个目标平台。

例如:

```

#include <hal.h>

int main() {
    while(1) {
        addr_write(0xa0, LEVEL_HIGH);
        wait_msec(1000);
        addr_write(0xa0, LEVEL_LOW);
        wait_msec(1000);
    }
}

```

这里，`hal.h`头文件将为每个目标平台实现——为特定的硬件提供专门的命令。每个平台的文件都将包含这两个函数。根据平台的不同，这个文件可能会为`wait_msec()`函数使用一个特定的硬件定时器，而`addr_write()`函数会使用一个包含外设寄存器和应用程序可以访问的所有内容的内存映射。

为特定目标编译应用程序时，可能需要在 Makefile 中提供目标参数，例如:

```

ifndef TARGET
$(error TARGET parameter not provided.)
endif

INCLUDES := -I targets/$(TARGET)/include/

```

这样，为一个特定的目标进行编译所需要的唯一事情就是为所述目标编写一个专门的文件，并将该目标的名称提供给 Makefile。

## 裸机或 HAL

前一节对于裸机编程或者没有固定 API 的类似情况非常有用。然而，软件库定义了一个固定的 API，抽象出底层硬件实现的细节，这种情况现在很普遍。这被称为硬件抽象层(HAL)，是操作系统的标准特性，无论是小型(RT)操作系统，还是成熟的桌面或分布式服务器操作系统。

就其核心而言，HAL 本质上与我们在上一节中定义的系统相同。主要区别在于它提供了一个可用于其他软件的 API，而不是 HAL 作为唯一的应用程序。扩展基本的 HAL，我们可以以驱动程序的形式添加诸如硬件支持的动态加载之类的特性。驱动程序本质上是它自己的小迷你 HAL，它抽象出它所支持的硬件的细节，同时实现它所需要的功能，以便被更高级的 HAL 调用。

一般来说，使用现有的或定制的 HAL 是非常可取的，即使是针对单个硬件平台。事实是，即使一个人只为一个微控制器编写代码，为了使用常规调试和代码分析工具，如 Valgrind 套件，能够在工作站 PC 的 HAL 上运行代码也有很多好处。

## 性能扩展不是免费的

除了“我的代码会运行吗？”这个问题，还有一个重要的考虑因素就是“效率会有多高？”。这对于涉及大量输入/输出(IO)操作、密集计算或长时间循环的代码尤其重要。从理论上讲，同样的代码在 16 MHz AVR 微控制器上的运行效果不如在 1.5 GHz 四核 Cortex-A72 片上系统上的运行效果，这是没有道理的。

然而，实际上，其含义远不止是时钟速度。是的，ARM 系统会抹杀 AVR MCU 的原始性能结果，但除非人们努力使用额外的三个内核，否则它们只会无所事事地坐在那里。假设目标平台有一个支持 C++11 标准的编译器，可以使用它内置的多线程支持(在<[线程](https://en.cppreference.com/w/cpp/header/thread) >头中)，基本程序如下所示:

```

#include <thread>
#include <iostream>

void f0(int& n) {
    n += 1;
}

int main() {
    int n = 1;
    std::thread t0(f0, std::ref(n));
    t0.join();
    std::cout << "1 + 1 = " << n << std::endl;
}

```

如上所述，这段代码可以在任何具备必要 STL 功能的 C++11 编译器上运行。当然，这里的主要问题是，为了像这样支持多线程，需要有一个 HAL 和调度程序来实现这样的功能。这就是使用像 [FreeRTOS](https://www.freertos.org/) 或 [ChibiOS](http://www.chibios.org) 这样的实时操作系统可以省去你很多麻烦的地方，因为它们预装了所有这些功能。

如果你不希望在一个 8 位的 MCU 上塞满一个 RTOS，那么根据目标，总是可以选择使用 RTOS API 或者之前提到的裸机(定制)HAL。这完全取决于代码的可移植性和可伸缩性。

## 小心洗牌

前面提到的 Cortex-A72 是一种无序设计，这意味着编译器生成的代码将被处理器动态重组，因此可以以任何顺序执行。执行代码的处理器越快越先进，潜在的问题就越多。根据目标平台的支持，应该使用处理器原子来隔离指令。对于 C++11，这些可以在 STL 的<[原子](https://en.cppreference.com/w/cpp/header/atomic) >头文件中找到。

这意味着在关键指令之前和之后添加指令，通知处理器所有这些指令属于一个整体，应该作为一个单元执行。这确保了例如在 32 位处理器上的 64 位整数计算将在 64 位处理器上同样工作，即使前者需要分多个步骤来完成。如果没有防护指令，另一条指令可能会导致原始 64 位整数的值被修改，从而破坏结果。

虽然互斥、自旋锁、rw 锁和 kin 在过去更常用于处理这种关键操作，但过去几十年的趋势是走向无锁设计，这种设计往往更有效，因为它们直接与处理器一起工作，开销很小，不像互斥需要额外的状态和操作集来维护。

## 在 HAL 之后，操作系统抽象层

标准最棒的一点是人们可以有很多标准。这也是几十年来操作系统(OS)所发生的事情，每个操作系统都开发了自己的 HAL、内核 ABI(用于驱动程序)和面向应用的 API。对于编写驱动程序，可以创建一个所谓的粘合层，将驱动程序的业务逻辑映射到内核的 ABI 调用，反之亦然。这基本上就是 Linux 中的 NDIS 包装器所做的事情，它允许最初为 Windows NT 内核编写的 WiFi 芯片组驱动程序在 Linux 下使用。

对于 userland 应用程序，情况类似。由于每个操作系统都提供自己独特的 API 来编程，这意味着人们必须以某种方式将它包装在一个粘合层中，以使它能够跨操作系统工作。当然，您可以自己完成这项工作，在编译库或应用程序时，为所请求的目标操作系统创建一个包含特定头文件的库，就像我们在本文开头看到的那样。

然而，更容易的是使用提供这种功能的无数现有库中的一个。在这里，GTK+、WxWidgets 和 Qt 一直是最受欢迎的，当不需要图形用户界面时， [POCO](http://pocoproject.org/) 非常受欢迎。

## 展现极致便携性

根据项目的不同，人们可以在从 ESP8266 或 STM32 MCU 到高端 AMD PC 的所有设备上运行完全相同的代码，只需要重新编译。这是我自己的一些项目的重点，NymphCast 是这方面最突出的。这里，客户端控制器使用一个远程过程调用(RPC)库: [NymphRPC](https://github.com/MayaPosch/NymphRPC) 。

由于 NymphRPC 是使用 [POCO 库](https://pocoproject.org/)编写的，所以前者可以在 POCO 支持的任何平台上运行，几乎是任何嵌入式、桌面或服务器操作系统。不幸的是，POCO 目前还不支持 FreeRTOS。然而，FreeRTOS 支持 NymphRPC 工作所需的所有常见多线程和网络 API，允许编写 FreeRTOS 端口，该端口使用 POCO 中特定于 FreeRTOS 的粘合层来映射这些 API。

在此之后，只需进行简单的重新编译，就可以使 nympcast 客户端软件(和 NymphRPC)在 FreeRTOS 支持的任何平台上运行，从而允许用户从 PC 到智能手机到 ESP8266 或类似的支持网络的 MCU 控制 nympcast 服务器，而无需更改核心逻辑。

## 未来是光明的(在 CLI 上)

尽管 C++标准不幸错过了在 C++20 标准中添加网络支持[，但我们仍然可以在 C++23 中看到它。有了这种直接在语言的标准库中的功能，拥有支持目标平台的 C++23 编译器将意味着人们可以为 FreeRTOS、Windows、Linux、BSD、MacOS、VxWorks、QNX 等等编译相同的代码。所有这些都不需要额外的库。](https://hackaday.com/2019/07/30/c20-is-feature-complete-heres-what-changes-are-coming/)

当然，GUI 编程是一个很大的例外。例如，网络总是非常接近 Berkeley 风格的套接字，多线程在不同的实现中也相当一致。但是跨操作系统的图形用户界面，甚至是 Linux 和 BSD 上的 XServer 和 Weyland 的单个窗口管理器之间的图形用户界面是非常不同和复杂的。

出于这个原因，大多数跨平台 GUI 库甚至懒得使用这些 API，而是创建一个简单的窗口，并在其上呈现自己的小部件，有时近似于本机 UI 的外观。同样流行的是滥用 HTML 之类的东西，并使用它来近似 GUI，添加或不添加自己的 HTML 渲染引擎和 JavaScript 运行时。

显然，对于跨平台开发来说，GUI 仍然是最后的前沿。在其他方面，我们已经取得了长足的进步。