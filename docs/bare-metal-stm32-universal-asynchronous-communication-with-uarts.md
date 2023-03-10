# 裸机 STM32:通用异步 UARTs 通信

> 原文：<https://hackaday.com/2021/01/08/bare-metal-stm32-universal-asynchronous-communication-with-uarts/>

MCU 上最基本也是最通用的通信接口之一是 UART，即通用异步收发器。通常以 UART 或 USART 的形式出现，前者允许纯异步串行通信，而后者增加了流量控制。当使用 MCU 时，它们也是输出调试信息的最常见方式之一。

虽然与 GPIO 外设相比，设置和使用起来有些棘手，但 ST 的 STM32 系列的美国艺术产品使用起来相当简单，并立即提供了一种与设备进行双向通信的简单方法。在本文中，我们将了解如何在 STM32 微控制器上开始基本的 UART 通信。

## 挑一个，任何一个

使用哪个 USART 外设似乎是一个非常简单的选择，尤其是当低端 STM32F0 MCUs 只有两个 USART 时。也就是说，直到你意识到它们并不完全相同。虽然它们都支持基本的 UART 功能，但有些增加了 USART 支持，有些具有 IrDA 和智能卡模式。

![](img/b5c889a5ec7c2a49d8069f05e862ed0e.png)

USART features on the STM32F051 MCU.

STM32F051 数据手册中的列表显示，这两种外设截然不同，只有第一种外设具有许多高级功能，相比之下，第二种外设相当简单。这是我们在 STM32 外设中经常看到的，不仅仅是 USARTs，尤其是定时器。根据个人需求选择合适的外设可能至关重要，因此知道您需要哪些功能是一项重要的技能。

就我们的目的而言(没有 DMA 的基本 UART)，几乎什么都可以，但如果我们后来想添加智能卡阅读器功能，或者决定自动波特率检测将是方便的，我们会希望记住这一点。特别是在为定制硬件设计时，如果您需要在以后的阶段进行更改，或者使产品的进一步开发变得更加复杂，为它们选择外设集和相关引脚可能会适得其反。

## 打开它

与其他外设一样，在启动时，USART 外设不通电。要改变这种情况，我们必须在外设所在总线的相应 RCC(复位和时钟控制)寄存器中切换一个位。例如，如果我们想在 STM32F0 MCU 上使用 USART1，当我们查看相关 MCU 的参考手册(RM)中的 RCC 时钟使能寄存器时，可以看到它位于 APB2 总线上，本例中为 RCC_APB2ENR:

[![](img/1257074f56e421c24df04c269f2453c0.png)](https://hackaday.com/wp-content/uploads/2020/11/stm32f042_rcc_apb2enr-rethemed.png)

RCC_APB2ENR on STM32F042 (RM0091 6.4.7).

通过将“1”写入位 14，USART1 外设的时钟域将被启用，我们可以使用其寄存器。但是，此时外设尚未配置和启用(活动)。为了做到这一点，我们必须再完成几个步骤:

*   启用 GPIO 组，我们希望使用它的管脚与外界通信。
*   在 USART_BRR 中设置波特率。
*   使用内部时钟寄存器使能 USART 外设。
*   可选地配置中断。

## 在功能之间交替

通用 I/O (GPIO)外设不只有一种功能。作为“通用”设计的一部分，它们的接线不仅允许数字 I/O，还允许连接到中断控制器(EXTI)和其它外设，包括 USARTs、ADC、DAC 等:

![](img/868a48deab78c12a77f7310f9396432c.png)

Basic I/O port pin structure on F0 MCUs. (RM0091 8.3).

由于我们希望将 USART1 外设与外界相连，因此需要在我们希望使用的引脚上启用备用功能(AF)模式。为此我们需要两样东西:

*   MCU 可以将哪些引脚作为此功能的目标。
*   一种在引脚上设置此 AF 模式的方法。

对于 STM32F0，F4，F7 和相关的家庭，这是相当直接的。首先，我们需要查看 MCU 数据手册中的替代功能映射表。例如，对于 STM32F042 MCU 上的 USART1，我们查看其数据手册第 4 节(*“引脚排列和引脚描述”*)的第 5 版(此处为 2017 年[版)，在表 14 中，我们看到了端口 A 的以下 AF 模式:](https://www.st.com/en/microcontrollers-microprocessors/stm32f0-series.html#documentation)

[![](img/5c6f5d028fb8b0a66d6a23ce842b78c8.png)](https://hackaday.com/wp-content/uploads/2021/01/stm32f042_pa9_pa10_af-rethemed-with-header.png)

AF modes on PA9 and PA10 for STM32042 MCUs.

标有 AF[0..7]用于替代功能 0 至 7。我们可以看到，通过 AF1，我们可以将 USART1 的 TX 和 RX 引脚用于端口 A 的引脚 9 和 10。我们现在只需要一种方法来设置它，使用 GPIO 外设的 AFRL 和 AFRH 寄存器来完成。这分别代表*‘交替功能寄存器低’*和*‘交替功能寄存器高’*，GPIO 组的 16 个引脚的一半被分配到这些寄存器中的每一个。

由于我们对引脚 9 和 10 感兴趣，我们想将 GPIO_AFRH 中的 AFSEL9 和 AFSEL10 的值都更改为 AF1 (0x1):

![](img/b00649a496e5f5addb0fcfab9f2c5afc.png)

GPIO_AFRH on STM32F042 with AF values.

完成后，我们就可以配置 USART 外设了，只需简单了解一下 STM32F1 AF 配置即可。

## 小心豹子

虽然 STM32F1 系列 MCU 有很多积极的方面，但它们的 GPIO 外设不在此列。当观察在 GPIO 引脚上配置 AF 模式时，其原因再次变得显而易见。比方说，我们希望在 STM32F103 MCU 上配置 AF 模式，首先查看参考手册(RM0008)的第 9.3 节(*“备用功能 I/O 和调试配置(AFIO)’*)，然后翻到第 9.3.8 节(*“USART 备用功能重新映射”*)，选择我们最喜欢的 USART 表(USART1，表 54)，得到:

![](img/11ea3466b8d01edfe8169a697eed393d.png)

STM32F103 USART remapping (RM0008 9.3.8, table 54).

由于 STM32F103 上有限的多路复用结构，这里没有一层又一层的交替功能模式，只是一个简短的“非此即彼”的问题。看起来不算太糟，对吧？有趣的是，AF 功能并没有完全集成到 GPIO 外设中，而是位于 AFIO 中。浏览第 9.4.2 节，我们会发现 AFIO_MAPR(重映射寄存器)，我们应该在其中切换相关条目(USART1_REMAP):

![](img/da87c04840d9a96a122f92bfd8efeda9.png)

AFIO_MAPR on STM32F103 (RM0008 9.4.2).

虽然这似乎没有现代 STM32 方法复杂，但令人恼火的是，AF 模式与外设相关，而不是与 GPIO 引脚相关。在 F1 MCUs 上，您不必使用端口、引脚号和所需的 AF 目标在 GPIO_AFRH 或 GPIO_AFRL 中选择 AF 模式，而是必须知道外设及其在 AFIO_MAPR 的入口位置，以及与这些入口和外设相关联的引脚。

## USART 配置

概括地说，此时我们仍然必须设置 UART 的波特率，并在发送“Hello World”之前启用 UART。设置波特率自然不像在 USART_BRR 寄存器中设置所需的数字那么简单:

![](img/14bada08c68e5d8ab9d802925da78424.png)

STM32F0 USART_BRR layout. (RM0091 27.8.4)

不涉及太多细节(例如参见 RM0091 中的 27.5.4)，在不改变默认设置的情况下填充该寄存器的简单方法(如在 USART_CR1 中使能 8 上的*)是将系统内核时钟除以所需波特率，然后将其除以 16 两次，首先获得整数分数，然后使用[模](https://en.wikipedia.org/wiki/Modulo_operation)运算获得余数(错误地称为 st 的“尾数”)。*

在代码中:

```

uint16_t uartdiv = SystemCoreClock / baudrate;
instance.regs->BRR = (((uartdiv / 16) << USART_BRR_DIV_MANTISSA_Pos) |	((uartdiv % 16) << USART_BRR_DIV_FRACTION_Pos));

```

这里，波特率是所需的波特率(例如 9600)，SystemCoreClock 是以 Hz 为单位的核心系统时钟速度。使用 USART_BRR 中“尾数”和“分数”位置的位置，它们的值被移位成整数值，然后被写入寄存器。

完成所有的艰苦工作后，我们现在可以启用 USART 了。这是在 USART_CR1 寄存器中完成的:

![](img/1f1907465729460ca8857f9333a7d257.png)

USART_CR1 on STMF0\. (RM0091 27.8.1)

这里切换到‘1’的位是 **RE** (接收使能) **TE** (发送使能) **UE** (USART 使能)和 **RXNEIE** (RXNE 中断使能)。最后一个使能新数据到达时产生中断，对于基本 UART 操作是可选的。此时，我们应该能够分别通过写入或读取 GPIO_DR 来发送和接收数据。

## 该说“嗨”了

利用 UART 发送和接收数据的核心是 USART_SR(状态寄存器):

![](img/7e5880029e9cae2112eed272cc2f31ed.png)

STM32F0 USART_SR register layout. (RM0091 27.6.1)

这里需要注意的是:

*   **TXE** (发送数据寄存器为空)。
*   **RXNE** (接收数据寄存器不为空)。

第一个(TXE)将在每次我们希望发送一个字节时进行检查:

```

while (!(instance.regs->SR & USART_SR_TXE)) {};
instance.regs->DR = (uint8_t) ch;

```

反之亦然，要读取数据，我们需要检查后者(RXNE ),以了解数据是否可供读取:

```

if (instance.regs->SR & USART_SR_RXNE) {
    rxb = instance.regs->DR;
    instance.callback(rxb);
}

```

这些代码片段取自 Nodate 框架中的 [USART 类](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/cpp/core/src/usart.cpp)。

## 包扎

以这种方式接收和发送单字节并不是使用 UART 的最佳方式。在接下来的文章中，我们将探讨如何添加中断、DMA 传输和控制流(USART)等功能，以充分利用这些 USART 外设的多功能性。

虽然其核心看似简单，但 USARTs 可以被视为通信外设的瑞士军刀。它们几乎可以在任何地方工作，可以适应各种各样的任务，无论是需要连接传感器，提供用户界面，控制工业设备，还是更具异国情调的东西。希望这篇文章能让你对这些可能性有所了解。