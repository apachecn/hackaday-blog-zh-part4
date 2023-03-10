# 裸机 STM32:在主收发器模式下使用 I2C 总线

> 原文：<https://hackaday.com/2022/05/11/bare-metal-stm32-using-the-i2c-bus-in-master-transceiver-mode/>

作为当今最受欢迎的系统内板载和板间通信总线之一，您很有可能最终将它用于嵌入式系统。I2C 提供多种速度，同时只需要两条线(时钟和数据)，这使得它比 SPI 等替代方案更容易处理。在 STM32 系列 MCU 中，每个设备上至少有一个 I2C 外设。

作为一种共享的半双工介质，I2C 使用一种相当简单的呼叫-响应设计，其中一台设备控制时钟，其它设备只是等待和监听，直到它们的固定地址被发送到 I2C 总线上。虽然配置 STM32 I2C 外设需要几个步骤，但之后使用起来却很轻松，我们将在本文中看到这一点。

## 基本步骤

假设传感器等接收设备连接正确，必要的上拉电阻到位，接下来我们可以开始配置 MCU 的 I2C 外设。我们将使用 STM32F042 作为目标 MCU，但从 I2C 的角度来看，其他 STM32 系列非常相似。我们还将使用 CMSIS 风格的外设和寄存器引用。

首先，我们设置希望用于 I2C 外设的 GPIO 引脚，启用适当的备用功能(AF)模式。这记录在目标 MCU 的数据手册中。对于 STM23F042 MCU，标准 SCL(时钟)引脚在 PA11 上，带 AF 5。SDA(数据)位于 PA12 上，具有相同的 AF。为此，我们需要在 GPIO_AFRH(替代功能寄存器高电平)寄存器中设置适当的位:

[![](img/b00649a496e5f5addb0fcfab9f2c5afc.png)](https://hackaday.com/wp-content/uploads/2020/11/stm320f42_gpio_afrh-rethemed.png)

GPIO_AFRH on STM32F042 with AF values.

通过为引脚 11 和 12 (AFSEL11 和 AFSEL12)选择 AF 5，这些引脚然后在内部连接到第一个 I2C 外设(I2C1)。这类似于我们在关于 UART 的[上一篇文章中所做的。我们还必须在 GPIO_MODER 中使能引脚的 AF 模式:](https://hackaday.com/2021/01/08/bare-metal-stm32-universal-asynchronous-communication-with-uarts/)

[![](img/9b72e92ab517df9a758227f1f17075a0.png)](https://hackaday.com/wp-content/uploads/2021/04/stm32f0x2_gpio_moder.png)

STM32F0x2 GPIO_MODER layout (RM0091, 8.4.4).

所有这些都是使用以下代码完成的:

```

uint8_t pin = 11;                // Repeat for pin 12
uint8_t pin2 = pin * 2;
GPIOA->MODER &= ~(0x3 << pin2); 
GPIOA->MODER |= (0x2 << pin2);   // Set AF mode.

// Set AF mode in appropriate (high/low) register.
if (pin < 8) { 
    uint8_t pin4 = pin * 4; 
    GPIOA->AFR[0] &= ~(0xF << pin4); 
    GPIOA->AFR[0] |= (af << pin4); 
} 
else { 
    uint8_t pin4 = (pin - 8) * 4; 
    GPIOA->AFR[1] &= ~(0xF << pin4); 
    GPIOA->AFR[1] |= (af << pin4);
}

```

请注意，我们希望 GPIO 寄存器中的 SCL 和 SDA 引脚都配置为悬空状态，没有上拉或下拉，并且为开漏配置。这与 I2C 公共汽车的特性相匹配，该公共汽车被设计成排水明沟。实际上，这意味着总线上的上拉电阻会使信号保持高电平，除非总线上的主机或从机将其拉低。

第一个 I2C 外设的时钟在`RCC_APB1ENR`(使能寄存器)中通过以下方式使能:

`RCC->APB1ENR |= RCC_APB1ENR_I2C1EN;`

一些 STM32F0 MCUs 只有一个 I2C 外设(STM32F03x 和 F04x)，而其他的有两个。不管怎样，如果 I2C 外设存在，在该寄存器中设置其时钟使能位之后，我们现在可以继续将 I2C 外设本身配置为主机。

## 时钟配置

在对 I2C 外围设备执行任何其他操作之前，我们必须确保它处于禁用状态:

`I2C1->CR1 &= ~I2C_CR1_PE;`

时钟设置在`I2C_ TIMINGR`中设定:

[![I2C_TIMINGR layout, as per RM0091 (26.7.5)](img/2e73a194183f93cd350da635bbecd886.png)](https://hackaday.com/wp-content/uploads/2022/04/stm32_f0_i2c_timingr.png)

I2C_TIMINGR layout, as per RM0091 (26.7.5)

《参考手册》根据 I2C 时钟列出了许多带有时序设置的表格，例如，对于 STM32F0 上的 8 MHz I2C 时钟速度:

[![IC2_TIMINGR configuration example table. Source: RM0091, 26.4.10.](img/999ebadd91ff9d995cdf8ab16d195f5f.png)](https://hackaday.com/wp-content/uploads/2022/04/stm32_f0_i2c_timing_setting_example_8_MHz.png)

IC2_TIMINGR configuration example table. Source: RM0091, 26.4.10.

通过将这些值按正确的顺序插入到 I2C 计时寄存器中，可以将该表转换为一个现成的值数组，以配置 I2C 外设，例如 STM32F0:

```

uint32_t i2c_timings_4[4];
uint32_t i2c_timings_8[4];
uint32_t i2c_timings_16[4];
uint32_t i2c_timings_48[4];
uint32_t i2c_timings_54[4];

i2c_timings_4[0] = 0x004091F3;
i2c_timings_4[1] = 0x00400D10;
i2c_timings_4[2] = 0x00100002;
i2c_timings_4[3] = 0x00000001;
i2c_timings_8[0] = 0x1042C3C7;
i2c_timings_8[1] = 0x10420F13;
i2c_timings_8[2] = 0x00310309;
i2c_timings_8[3] = 0x00100306;
i2c_timings_16[0] = 0x3042C3C7;
i2c_timings_16[1] = 0x30420F13;
i2c_timings_16[2] = 0x10320309;
i2c_timings_16[3] = 0x00200204;
i2c_timings_48[0] = 0xB042C3C7;
i2c_timings_48[1] = 0xB0420F13;
i2c_timings_48[2] = 0x50330309;
i2c_timings_48[3] = 0x50100103;
i2c_timings_54[0] = 0xD0417BFF;
i2c_timings_54[1] = 0x40D32A31;
i2c_timings_54[2] = 0x10A60D20;
i2c_timings_54[3] = 0x00900916;

```

此处可用的其他选项是让意法半导体提供的工具(如 CubeMX)为您计算这些值，或者使用参考手册中的信息自行计算。此时，STM32 的 Nodate 框架 [I2C 实现](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/cpp/core/src/i2c.cpp)使用了两者，STM32F0 的预定义值与其他系列的动态计算值相同。

动态计算定时值的优点是它不依赖于预定义的 I2C 时钟速度。缺点是在计算这些值时会有额外的延迟，而不是直接从表中读取。哪种方法最有效取决于项目的需求。

通过如此配置`I2C_TIMINGR`寄存器，我们可以启用外设:

`I2C1->CR1 |= I2C_CR1_PE;`

## 写入数据

随着 I2C 外围设备准备就绪，我们可以开始发送数据。与 USART 非常相似，这是通过写入传输(TX)寄存器并等待传输完成来实现的。《参考手册》中提供的有用流程图涵盖了以下步骤:

[![Master transmitter flowchart, reproduced from RM0091.](img/c02b26c99a31da55bf7af9ce6af6d015.png)](https://hackaday.com/wp-content/uploads/2022/04/stm32_f0_i2c_transmission_flowchart_255_bytes.png)

Master transmitter flowchart, reproduced from RM0091.

这里值得注意的是，对于某些检查，如 I2C_ISR_TC(传输完成)，其思想不是检查一次就完成，而是等待一个超时。

对于 1 字节的简单传输，我们将 I2C_CR2 设置为:

```

I2C1->CR2 |= (slaveID << 1) | I2C_CR2_AUTOEND | (uint32_t) (1 << 16) | I2C_CR2_START;

```

这将启动总共 1 个字节的传输(左移至 I2C_CR2 寄存器中的 NBYTES 位置)，目标是 7 位`slaveID`，自动产生 I2C 停止条件。传输完成(NBYTES transferred)后，生成 STOP，它在 I2C_ISR 中设置一个名为 STOPF 的标志。

当我们知道已经完成数据传输时，我们必须等待该标志被置位，然后清除 CR2 的标志，并清除 I2C CR2 寄存器:

```

instance.regs->ICR |= I2C_ICR_STOPCF;
instance.regs->CR2 = 0x0;

```

这就完成了基本的数据传输。要传输多个字节，只需循环相同的程序，每个周期向`I2C_TXDR`写入一个字节，并等待`I2C_ISR_TXIS`置位(需要超时)。要传输超过 255 字节的数据，在 I2C_CR2 中设置`I2C_CR2_RELOAD`而不是`I2C_CR2_AUTOEND`将允许传输新的一批 255 字节或更少的数据。

## 阅读日期

从设备读取数据时，确保中断被禁用(使用`NVIC_DisableIRQ`)。一般来说，读请求由微控制器发送到器件，器件通过发送所请求的寄存器内容作为回复来响应。例如，如果 BME280 MEMS 传感器作为唯一有效载荷发送 *0xd0* ，它将通过发回其(固定)ID(在工厂编程写入该寄存器)来做出响应。

从设备接收的基本流程图如下:

[![Master receiver flowchart for STM32F0\. Source: RM0091.](img/64fdffecbd6a6340e7d76cd35c32f722.png)](https://hackaday.com/wp-content/uploads/2022/04/stm32_f0_i2c_reception_flowchart_255_bytes.png)

Master receiver flowchart for STM32F0\. Source: RM0091.

这里的基本思想与传输数据是一样的。我们以与之前相同的方式配置 I2C CR2。这里的主要区别是，我们等待 I2C_ISR_RXNE 标志复位，之后我们可以将 I2C_RXDR 的单字节内容读入我们的缓冲区。

就像写数据一样，在读取 NBYTES 之后，我们必须等待 I2C_ISR_STOPF 标志被置位，然后通过 I2C_ICR 寄存器和 I2C_CR2 寄存器将其清零。

## 基于中断的读取

用 I2C 设置中断要求我们激活相关 I2C 外设的中断。这必须在外设处于禁用状态时完成。之后，我们可以启用中断:

```

NVIC_SetPriority(I2C1_IRQn, 0);
NVIC_EnableIRQ(I2C1_IRQn);

```

然后通过设置配置位在外设上使能中断:

```

I2C1->CR1 |= I2C_CR1_RXIE;

```

确保正确命名的中断处理程序(ISR)以启动代码中指定的名称实现:

```

volatile uint8_t i2c_rxb = 0;

void I2C1_IRQHandler(void) {
    // Verify interrupt status.
    if ((I2C->ISR & I2C_ISR_RXNE) == I2C_ISR_RXNE) {
        // Read byte (which clears RXNE flag).
        i2c_rxb = instance.regs->RXDR;
    }
}

```

如果使用 C 以外的语言，不要忘记在处理程序周围添加`extern "C" { }`块，以防止函数名混乱。

有了这段代码，每次读缓冲区接收到一个字节，ISR 就会被调用，我们可以将它复制到缓冲区或其他地方。

## 多设备使用

从这一点可以推测，使用单个微控制器收发器的多个器件只需要在任何有效载荷之前发送正确的器件标识符。这也是清零 I2C_CR2 寄存器并在下一个发送或接收周期正确置位以防止器件标识符混淆的关键所在。

根据代码实现(例如多线程 RTOS)，可能会发生读写冲突。在这种情况下，协调 I2C 的写入和读取非常重要，这样就不会丢失数据或命令，也不会将数据或命令发送到错误的设备。

## 包扎

一旦扫清了设置时钟配置的障碍，在 STM32 上使用 I2C 并不复杂。这是一个值得单独写一篇文章的主题，还有一些关于 I2C 的高级主题，比如时钟拉伸和噪声过滤。默认情况下，STM32 MCUs 上的 I2C 外设在其 I2C 输入上启用了噪声滤波器，但也可以进一步配置。

对于 I2C 来说，基本的读写很容易，但仍然有一个完整的兔子洞需要探索，当涉及到在 STM32 上实现自己的 I2C 设备时也是如此。请继续关注关于这些主题的更多文章。