# Newlib 嵌入式 C 标准库及其使用方法

> 原文：<https://hackaday.com/2021/07/19/the-newlib-embedded-c-standard-library-and-how-to-use-it/>

为新的硬件平台编写代码时，您最不想做的事情就是为 I/O 例程、字符串处理和其他与实际项目无关的类似繁琐的细节而烦恼。在更大的系统上，这是 C 标准库传统上发挥作用的地方。

对于像微控制器这样的小型嵌入式平台，资源通常非常紧张，完全成熟的 stdlib 不适合，这就是为什么 [Newlib](https://sourceware.org/newlib/) 存在的原因:将标准库的可移植性优势带给微控制器。

无论你是用 C、C++还是 MicroPython 来编写一个 MCU，Newlib 很可能就在引擎盖下。然而，它究竟是如何与硬件集成的，例如，文件和输入/输出处理的系统调用(系统调用)是如何实现的？

## 一个粗短的工具包

C 标准库提供了许多包含可用功能的头文件。随着 C 标准的每一次修订，都添加了新的头文件，涵盖了更多的特性。在这些原始标题中，最常用的包括:

*   <stdio.h></stdio.h>

*   <stdlib.h></stdlib.h>
*   <math.h></math.h>

这里，人们已经可以推测，这些头部中的每一个在将底层代码移植到新平台的复杂程度上是不同的，尤其是在没有操作系统(OS)的 MCU 平台的情况下。没有操作系统，就没有明显的方法来提供对某些功能的简单访问，比如标准文本输入和输出，或者系统时钟和日历。这让我们想到了 Newlib 中的许多[存根函数。](https://sourceware.org/newlib/libc.html#Stubs)

在<string.h>的情况下，我们非常安全，因为 [C 风格的字符串](https://en.wikipedia.org/wiki/C_string_handling)和它们的操作本质上涉及内存操作，这不需要特殊的系统调用。这与< stdio.h >非常不同，后者包含与文件访问和操作相关的功能，以及标准输出或输入的输入和输出。</string.h>

如果没有一些将 libc 实现连接到终端或存储介质的底层代码，这些 I/O 特性就不会发生任何事情，因为对于`printf()`或`fopen()`没有合理的默认动作。如果我们希望使用`printf()`或其他文本输出函数，Newlib 文档[告诉我们](https://sourceware.org/newlib/libc.html#Stubs)我们需要实现一个全局函数`int _write(int handle, char* data, int size)`。

正如名字“stub”所暗示的，Newlib 库自带了自己的 stub 实现，它什么也不做，那么我们该怎么做才能让`printf()`写到某个合理的地方呢？这里要认识到的最重要的事情是，这完全依赖于实现，什么有意义取决于具体的项目。通常，在嵌入式应用程序中，格式化的文本输出函数将用于输出调试和类似的信息，例如，在这种情况下，输出到 USART 非常有意义。

在我的 Nodate 框架中，选择的方法是允许代码在启动时选择一个特定的 USART 外设来发送输出，正如我们可以在 [IO 模块](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/cpp/core/src/io.cpp)中看到它的存根函数的实现:

```

bool stdout_active = false;
USART_devices IO::usart;
int _write(int handle, char* data, int size) {
	if (!stdout_active) { return 0; }

	int count = size;
	while (count-- > 0) {
		USART::sendUart(IO::usart, *data);
		data++;
	}

	return size;
}

```

提供了一个字符数组及其长度，然后我们将它传递给活动的 USART。由于 USART 传输单个字节，所以提供的数组一次传输一个字节。

由于目标 USART 可以在每个平台上改变，这是可配置的，允许开发者在启动时设置目标输出设备，以及在运行时动态设置。

```

bool IO::setStdOutTarget(USART_devices device) {
	IO::usart = device;	
	stdout_active = true;

	return true;
}

```

这些存根实现的重要之处在于，它们依赖 C 风格的链接来查找覆盖。因为在像 C++这样的语言中，名字管理是默认应用的，所以一定要在完整实现或者存根实现的前向声明周围应用一个`extern "C" { }`块。

## 时机的问题

为了让与时间相关的功能按照 [< time.h >](https://en.wikipedia.org/wiki/Time.h) 中的定义工作，需要有一个底层的时基，或者至少有一个计数器，我们可以从中获取这些信息。使用包含自启动以来的毫秒数的 systick 计数器不足以覆盖例如`time()`，其需要自 Unix 纪元以来的秒数。

底层`int _times(struct tms* buf)`系统调用的一个可能实现将使用系统的实时时钟(RTC)。这与使用 systick 相比还有一个主要优势，即 RTC 可以在低功耗模式下运行，即使系统定期进入睡眠模式甚至完全关闭，也能获得精确的时序结果。

在 Nodate 中，该功能在 STM32 的 [clock.cpp](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/cpp/core/src/clock.cpp) 中实现，如果 RTC 尚未启动，则启用 RTC:

```

int _times(struct tms* buf) {
#if defined RTC_TR_SU
	if (!rtc_pwr_enabled) {
		if (!Rtc::enableRTC()) { return -1; }
		rtc_pwr_enabled = true;
	}

	// Fill tms struct from RTC registers.
	// struct tms {
	//		clock_t tms_utime;  /* user time */
	//		clock_t tms_stime;  /* system time */
	//		clock_t tms_cutime; /* user time of children */
	//		clock_t tms_cstime; /* system time of children */
	//	};
	uint32_t tTR = RTC->TR;
	uint32_t ticks = (uint8_t) RTC_Bcd2ToByte(tTR & (RTC_TR_ST | RTC_TR_SU));
	ticks = ticks * SystemCoreClock;
	buf->tms_utime = ticks;
	buf->tms_stime = ticks;
	buf->tms_cutime = ticks;
	buf->tms_cstime = ticks;

	return ticks; // Return clock ticks.
#else
	// No usable RTC peripheral exists. Return -1.
	return -1;
#endif 
}

```

在基于 STM32 Cortex-M 的 MCU(STM 32 f 1 除外)上，RTC 的寄存器包含 [BCD](https://en.wikipedia.org/wiki/Binary-coded_decimal) (二进制编码十进制)格式的时间计数，这要求将其转换为二进制代码，以便与使用`_times()`功能的任何代码兼容:

```

uint8_t RTC_Bcd2ToByte(uint8_t Value) {
	uint32_t tmp = 0U;
	tmp = ((uint8_t)(Value & (uint8_t)0xF0) >> (uint8_t)0x4) * 10;
	return (tmp + (Value & (uint8_t)0x0F));
}

```

## 微控制器的新功能

从技术上来说，Newlib 有两个版本:一个是常规的全脂库，另一个是低脂的纳米版本，由 ARM 在 2013 年明确为 Cortex-M MCU 创建。常规 Newlib 的一个主要缺点是它占用了相当大的空间，这对于 flash 存储和 SRAM 有限的特别小的 MCU 来说，很可能意味着即使一个简单的“Hello World”也可能太大而不适合。

当使用 GCC 为 STM32 或 SAM 等 MCU 平台进行编译时，可以通过添加[规格文件](https://gcc.gnu.org/onlinedocs/gcc/Spec-Files.html)来指示编译器链接这个新的 lib-nano，以便在带有`--specs=nano.specs`的链接器命令中使用。这个规范文件基本上确保了项目链接到 Newlib-nano 库，并使用适当的头文件。

正如 linked ARM 文章中所指出的，常规 Newlib 和 nano 版本之间的大小差异非常显著。对于一个以低级别 Cortex-M0 MCU 为目标的项目，例如总共具有 16kb flash 和 4kb SRAM 的 [STM32F030F4](https://www.st.com/content/st_com/en/products/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus/stm32-mainstream-mcus/stm32f0-series/stm32f0x0-value-line/stm32f030f4.html) ，使用常规的 Newlib 是不可能的，因为最终的固件映像将会填满 flash，然后是一些。使用 Newlib-nano 时，Nodate 提供的基本演示项目(例如 Blinky、Pushy)的大小约为 2 kB，因此可以轻松放入 Flash 和 RAM 中。

在这里，人们可以通过将 Newlib 附带的默认`printf()`实现替换为优化的实现来进一步节省空间，比如 [mpaland 的 printf 实现](https://github.com/mpaland/printf)。这个实现已经和 Nodate 一起使用，甚至在这些小的 M0 皮层 MCU 上也获得了全面的支持。

## 保持纯洁

当开发更多资源受限的微控制器时，实际上每个字节都很重要。由于大多数这些 MCU 是单核系统，它们不需要多线程支持，而多线程支持在使用多核系统(例如 STM32H7 系列)时会很方便。无论是否启用了可重入性，在构建项目之后检查项目的映射文件时都可以很容易地观察到这一点。

当人们看到像`impure_data`这样的条目和类似的符号条目时，通常包含在`lib_a-impure.o`或类似的条目中，可重入代码被链接进来，这在最坏的情况下会耗费数千字节的空间。通常这些代码是因为项目代码中使用的某些功能而被链接进来的，但也可能来自`atexit()`处理器。这个可重入特性的解释可以在 Newlib 文档中找到[。](https://sourceware.org/newlib/libc.html#Reentrancy)

直接分析地图文件或者使用诸如[地图查看器](https://github.com/govind-mukundan/MapViewer)(仅限 Windows)这样的工具可以帮助追踪这些依赖关系。一个建议是将标志 `-fno-use-cxa-atexit`添加到 GCC 编译标志中，这样它就不会使用退出处理程序的可重入版本。

## 包扎

显然，所有这些仅仅涵盖了集成和使用 Newlib 所需的基础知识。还有更多的 syscall 存根没有涉及到，文件处理 API 本身就值得一篇文章来讨论。当从本文所讨论的裸机系统转移到有操作系统的系统时，Newlib 的动态特性也会发生变化。

流程管理是由`getpid()`、`fork()`和其他存根函数涵盖的另一个主题。虽然即使是像`printf()`这样的基本功能，在这里也必须实现自己的代码看起来有些复杂，但这也凸显了这种方法的优势，因为它非常灵活，可以很容易地适应任何平台。这就是为什么 Newlib 从资源有限的单核 Cortex-M MCU 一直到大型多核系统(包括游戏控制台)都基本保持不变。

图书图片:[【威尔士国民议会】](https://www.flickr.com/photos/39069511@N03/14722128644)[“威尔士公共图书馆/Llyfrgelloedd Cyhoeddus yng Nghymru”](https://www.flickr.com/photos/39069511@N03)/Cynulliad Cymru根据 2.0CC 获得许可