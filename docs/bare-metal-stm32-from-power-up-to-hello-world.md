# 裸机 STM32:从加电到 Hello World

> 原文：<https://hackaday.com/2020/11/17/bare-metal-stm32-from-power-up-to-hello-world/>

有些人可能会问，为什么要只使用 ARM 工具链和 ST 微电子公司提供的数据手册和参考手册来编写像 STM32 系列这样的 Cortex-M 微控制器。如果你对这个问题的第一反应不是惊慌失措地奔向最近的紧急出口，那么可能是这个问题激起了你的兴趣。为什么呢？

毫无疑问，人们可以使用任何现有的框架来编写 STM32 MCU，无论是 ST HAL 框架、普通 CMSIS，还是更有 Arduino 味道的东西。然而，当一天结束时，一个人仍然完全依赖于框架的文档和它的开发者，这有什么意思呢？更简洁地说，如果 STM32 参考手册的内容看起来仍然像是胡言乱语，人们真的了解这个平台吗？

让我们来看看裸机 STM32 编程是如何工作的，让最基本的例子运行，好吗？

## 像个人电脑，只是不同

从根本上说，微控制器和基于英特尔或 AMD 的成熟计算机之间没有什么区别。一旦外部电源稳定下来，至少有一个 CPU 内核会被初始化，此时启动固件会从一个固定的位置读取。在你的桌面上，这是 BIOS。对于 MCU，这是从(通常)集成只读存储器(ROM)中的特定偏移开始存储的代码。接下来发生的一切都取决于这个代码。

一般来说，在这个启动代码中，我们需要做一些基本的事情，比如设置中断向量表和特定寄存器的基本内容。初始化堆栈指针(SP)是必不可少的，将 ROM 的某些部分复制到 RAM 并初始化一些寄存器也是必不可少的。最终调用 main 函数，类似于 BIOS 完成环境设置后启动 PC 的操作系统。

## 咄咄逼人的例子

可能最基本有用的例子是我在我的 [Nodate STM32 框架](https://github.com/MayaPosch/Nodate)中亲切地称之为“ [Pushy](https://github.com/MayaPosch/Nodate/blob/master/examples/stm32/pushy/src/pushy.cpp) ”。它比传统的“Blinky”例子更基本，因为它只使用复位&时钟控制(RCC)寄存器和基本 GPIO 外设。它所做的只是读取 GPIO 引脚的输入寄存器，并根据输入值调整输出，但仍然可以随意打开或关闭 LED:



|  | # 包括<gpio . h> |
|  |  |
|  |  |
|  | int main () { |
|  | //const uint 8 _ t led _ pin = 3；//Nucleo-f 042k 6:B 口，3 脚。 |
|  | // 常量 GPIO _ ports led _ PORT = GPIO _ PORT _ B； |
|  | //const uint 8 _ t led _ pin = 13；//STM 32 f 4-发现:D 口，13 号针(橙色) |
|  | // 常量 GPIO _ ports led _ PORT = GPIO _ PORT _ D； |
|  | //const uint 8 _ t led _ pin = 7；// Nucleo-F746ZG:端口 B，第 7 针(蓝色) |
|  | // 常量 GPIO _ ports led _ PORT = GPIO _ PORT _ B； |
|  | constuint 8 _ tled _ pin =13； // 蓝色药丸:C 口，13 号针。 |
|  | constGPIO _ ports led _ PORT = GPIO _ PORT _ C； |
|  |  |
|  | //const uint 8 _ t button _ pin = 1；// Nucleo-f042k6 (PB1) |
|  | // 常量 GPIO _ ports button _ PORT = GPIO _ PORT _ B； |
|  | //const uint 8 _ t button _ pin = 0；//STM 32 f 4-发现(PA0) |
|  | // 常量 GPIO _ ports button _ PORT = GPIO _ PORT _ A； |
|  | //const uint 8 _ t button _ pin = 13；// Nucleo-F746ZG (PC13) |
|  | // 常量 GPIO _ ports button _ PORT = GPIO _ PORT _ C； |
|  | constuint 8 _ tbutton _ pin =10；//蓝色药丸 |
|  | constGPIO _ ports button _ PORT = GPIO _ PORT _ B； |
|  |  |
|  | // 在 LED 管脚上设置管脚模式。 |
|  | GPIO::set _ output(led _ port，led_pin，GPIO _ PULL _ UP)； |
|  | GPIO::write (led_port，led_pin，GPIO _ LEVEL _ LOW)； |
|  |  |
|  | // 在按钮引脚上设置输入模式。 |
|  | GPIO::set _ input(button _ port，button_pin，GPIO _ FLOATING)； |
|  |  |
|  | // 如果按钮下拉到地(高到低)，按下时‘button _ down’为低。 |
|  | // 如果按钮上拉至 Vdd(低至高)，按下时‘button _ down’为高。 |
|  | uint 8 _ tbutton _ down； |
|  | 而 ( 1 ) { |
|  | button _ down =GPIO::read(button _ port，button _ pin)； |
|  | 如果 (button_down == 1 ) { |
|  | GPIO::write (led_port，led_pin，GPIO _ LEVEL _ HIGH)； |
|  | } |
|  | 否则 { |
|  | GPIO::write (led_port，led_pin，GPIO _ LEVEL _ LOW)； |
|  | } |
|  | } |
|  |  |
|  | 返回0； |
|  | } |

[view raw](https://gist.github.com/MayaPosch/d4b71ae6ba86f9e5e036d00dd8c9bacf/raw/97889641f4d72076597084b8f00d9f6208cd75cd/stm32_example_pushy_nodate.cpp) [stm32_example_pushy_nodate.cpp](https://gist.github.com/MayaPosch/d4b71ae6ba86f9e5e036d00dd8c9bacf#file-stm32_example_pushy_nodate-cpp) hosted with ❤ by [GitHub](https://github.com)

这里我们可以看到两个最明显的元素:第一个是被调用的`main()`函数，第二个是包含的 GPIO 模块。它包含一个静态 C++类，调用该类写入连接有 led 的 GPIO 输出，以及从另一个连接有按钮的输入读取。我们还可以看到，所谓的“Blue Pill”(STM 32 f 103 c 8)已定义了其引脚，但该示例还有一些预设，我们可以通过取消注释适当的行来更改。

[![](img/11258c5ae0c2963c26f31f5549c843d0.png)](https://hackaday.com/wp-content/uploads/2020/10/stm32f0xx_rcc_ahbenr.png)

STM32F0xx’s RCC_AHBENR register description in the RM.

那么 RCC 寄存器在这里起什么作用呢？顾名思义，它们控制 MCU 内的时钟域，实质上充当 MCU 各部分的开/关开关。例如，如果我们查看 [STM32F0xx 参考手册](https://www.st.com/resource/en/reference_manual/dm00031936-stm32f0x1stm32f0x2stm32f0x8-advanced-armbased-32bit-mcus-stmicroelectronics.pdf)(第 6.4 节)中的`RCC_AHBENR`寄存器描述，我们可以看到标记为`IOPAEN`(输入/输出端口 A 使能)的位，它切换 GPIO A 外设的时钟。其他 GPIO 外设也是如此。

如上图所示，`AHBENR` 表示`AHB`的使能寄存器，它是 MCU 内部的一条总线，处理器内核、SRAM、ROM 和外设都连接到这条总线:

[![](img/4233dc4716c3bfdd49cbd09d69be1d35.png)](https://hackaday.com/wp-content/uploads/2020/10/stm32f0xx_system_architecture.png)

STM32F0xx system architecture (RM section 2.1).

Arm [AMBA](https://en.wikipedia.org/wiki/Advanced_Microcontroller_Bus_Architecture) 规范涵盖了 AHB(高级高性能总线)和 APB(高级外设总线)。通常，AHB 是最快的总线，将处理器内核与 SRAM、ROM 和高速外设连接起来。速度较慢的外设放置在速度较慢的 APB 上，通过 AHB 到 APB 的桥接实现通信。

## 集合时间到了

如前所述，运行的第一个代码是启动代码。对于 STM32F042x6 单片机，拇指汇编程序[中的一个通用启动程序可以在这里](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/asm/stm32f0/startup_stm32f042x6.S)看到。这是 ST 提供的通用 ASM(例如 STM32F0xx 的[)以及 CMSIS 设备包。它初始化 MCU 并调用低级 CMSIS C 代码](https://github.com/STMicroelectronics/cmsis_device_f0)[中的`SystemInit()`函数，例如用于 STM32F0xx](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/cpp/core/src/stm32f0/system_stm32f0xx.c) 。

此`SystemInit()`功能将系统时钟寄存器复位到所需的复位状态:使用内部 HSI 振荡器，以默认速度。在`*libc*`设置例程(这里是 [Newlib](https://sourceware.org/newlib/) ，一个 C/C++支持库)之后，它最终启动`main()`函数:

```

bl main

```

这条指令意味着用链接分支[，导致执行跳转到指定的标签，本质上。在这一点上，我们坚定地站在了我们“咄咄逼人”的例子`main()`中。现在一切都由](https://www.keil.com/support/man/docs/armasm/armasm_dom1361289865686.htm) [GPIO 类](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/cpp/core/src/gpio.cpp)来完成。

## GPIO

我们调用的第一个类方法是`GPIO::set_output()`用使能的上拉电阻将某个引脚设置为输出。这也是我们遇到 STM32 系列之间第一个差异的地方，因为基于 Cortex-M3 的 F1 系列与较新的 F0、F4 和 F7 系列具有非常不同的 GPIO 外设。这意味着对于 STM32F1xx，我们必须将每个引脚的多个选项放入一个寄存器中:



|  | // 输入/输出寄存器分布在两个组合寄存器中(CRL，CRH)。 |
|  | 如果(销< 8 ) { |
|  | // 设置 CRL 寄存器(CNF &模式)。 |
|  | uint 8 _ tpinmode = pin *4； |
|  | uint 8 _ tpincnf = pinmode+2； |
|  |  |
|  | if(speed = = GPIO _ LOW){ instance。regs->-CRL&#124; =(0x 2<<pin mode)；} |
|  | elseT2 if(speed = = GPIO _ MID){ instance。regs->CRL&#124; =(0x 1<<pin mode)；} |
|  | elseT2 if(speed = = GPIO _ HIGH){ instance。regs->CRL&#124; =(0x 3<<pin mode)；} |
|  |  |
|  | if(type = = GPIO _ PUSH _ PULL){ instance。regs->CRL&= ~(0x 1<<pincnf)；} |
|  | elseT2 if(type = = GPIO _ OPEN _ DRAIN){ instance。regs->CRL&#124; =(0x 1<<pincnf)；} |
|  | } |
|  | 否则 { |
|  | //设置 CRH 寄存器。 |
|  | uint 8 _ tpinmode =(pin-8)*4； |
|  | uint 8 _ tpincnf = pinmode+2； |
|  |  |
|  | if(speed = = GPIO _ LOW){ instance。regs->-CRH&#124; =(0x 2<<pin mode)；} |
|  | elseT2 if(speed = = GPIO _ MID){ instance。regs->CRH&#124; =(0x 1<<pin mode)；} |
|  | elseT2 if(speed = = GPIO _ HIGH){ instance。regs->CRH&#124; =(0x 3<<pin mode)；} |
|  |  |
|  | if(type = = GPIO _ PUSH _ PULL){ instance。regs->CRH&= ~(0x 1<<pincnf)；} |
|  | elseT2 if(type = = GPIO _ OPEN _ DRAIN){ instance。regs->CRH&#124; =(0x 1<<pincnf)；} |
|  | } |

[view raw](https://gist.github.com/MayaPosch/2272560bbd38f4f882e3d80cfbd21c20/raw/ed944154c8a4b30aecc766c0c7e21fce168bef15/stm32_gpio_output_f1.cpp) [stm32_gpio_output_f1.cpp](https://gist.github.com/MayaPosch/2272560bbd38f4f882e3d80cfbd21c20#file-stm32_gpio_output_f1-cpp) hosted with ❤ by [GitHub](https://github.com)

但是对于其他提到的系列，我们为每个选项(模式、速度、上拉/下拉、类型)提供了不同的寄存器:



|  | uint 8 _ tpin 2 = pin *2； |
|  | instance . regs-> MODER & = ~(0x 3<<pin 2)； |
|  | instance . regs-> MODER &#124; =(0x 1<<pin 2)； |
|  |  |
|  | instance . regs-> PUPDR & = ~(0x 3<<pin 2)； |
|  | if (pupd == GPIO_PULL_UP) { |
|  | 实例。regs->PUPDR&#124; =(0x 1<<pin 2)； |
|  | } |
|  | elseif(pupd = = GPIO _ PULL _ DOWN){ |
|  | 实例。regs->PUPDR&#124; =(0x 2<<pin 2)； |
|  | } |
|  |  |
|  | if(type = = GPIO _ PUSH _ PULL){ |
|  | 实例。regs->OTYPER&= ~(0x 1<<pin)； |
|  | } |
|  | elseif(type = = GPIO _ OPEN _ DRAIN){ |
|  | 实例。regs->OTYPER&#124; =(0x 1<<pin)； |
|  | } |
|  |  |
|  | 如果(速度== GPIO_LOW) { |
|  | 执行处理。规则->&= ~(0x 3<pin 2)； |
|  | } |
|  | elseT2 if(speed = = GPIO _ MID){ |
|  | 执行处理。规则->&= ~(0x 3<pin 2)； |
|  | 执行处理。规则->&#124; =(0x 1<<pin 2)； |
|  | } |
|  | elseT2 if(speed = = GPIO _ HIGH){ |
|  | 执行处理。规则->&= ~(0x 3<pin 2)； |
|  | 执行处理。规则->&#124; =(0x 3<<pin 2)； |
|  | } |

[view raw](https://gist.github.com/MayaPosch/1a1c93c6113a28d8cda40f2799431ce7/raw/e5544cdc7f4db21ed9b2a3d843db832ebf9295ce/stm32_gpio_output_f0-4-7.cpp) [stm32_gpio_output_f0-4-7.cpp](https://gist.github.com/MayaPosch/1a1c93c6113a28d8cda40f2799431ce7#file-stm32_gpio_output_f0-4-7-cpp) hosted with ❤ by [GitHub](https://github.com)

使用[位操作](https://en.wikipedia.org/wiki/Bitwise_operations_in_C)通过位掩码操作设置目标位来设置寄存器中的选项。寄存器名称通常具有很强的描述性，例如`PUPDR`表示上拉下拉寄存器。

一个人喜欢哪种风格主要取决于个人的看法。然而，在设置 pin 作为输入的情况下，我更喜欢较新的 GPIO 外设风格，使用以下漂亮、紧凑的代码，而不是 STM32F1xx 复杂的恐怖秀:



|  | uint 8 _ tpin 2 = pin *2； |
|  | instance . regs-> MODER & = ~(0x 3<<pin 2)； |
|  | instance . regs-> PUPDR & = ~(0x 3<<pin 2)； |
|  | if (pupd == GPIO_PULL_UP) { |
|  | 实例。regs->PUPDR&#124; =(0x 1<<pin 2)； |
|  | } |
|  | 否则 { |
|  | 实例。regs->PUPDR&#124; =(0x 2<<pin 2)； |
|  | } |

[view raw](https://gist.github.com/MayaPosch/8b896e7f6bcaa74a407251661339fce6/raw/581a4921c35be90246f606c01852e7257a663830/stm32_gpio_input_f0-4-7.cpp) [stm32_gpio_input_f0-4-7.cpp](https://gist.github.com/MayaPosch/8b896e7f6bcaa74a407251661339fce6#file-stm32_gpio_input_f0-4-7-cpp) hosted with ❤ by [GitHub](https://github.com)

为了从输入引脚读取，我们参考该 GPIO 组的输入数据寄存器(`GPIO_IDR`):

```
|  | uint 32 _ tIDR = instance . regs->IDR； |
|  | out =(IDR > > pin)&1U；//读出想要的位。 |
```

[view raw](https://gist.github.com/MayaPosch/a84fb356eb096e3c435a50c0ec494d4f/raw/1ea30c525e1cb761cf968e1349f40db9eef04812/stm32_gpio_read.cpp) [stm32_gpio_read.cpp](https://gist.github.com/MayaPosch/a84fb356eb096e3c435a50c0ec494d4f#file-stm32_gpio_read-cpp) hosted with ❤ by [GitHub](https://github.com)

同样，当我们写入一个引脚时，我们使用输出数据寄存器(`ODR`):



|  | if(LEVEL = = GPIO _ LEVEL _ LOW){ |
|  | 实例。regs->ODR&= ~(0x 1<<pin)； |
|  | } |
|  | elseT2 if(LEVEL = = GPIO _ LEVEL _ HIGH){ |
|  | 实例。regs->ODR&#124; =(0x 1<<pin)； |
|  | } |

[view raw](https://gist.github.com/MayaPosch/2e4d761821350867cb05016f129f86c7/raw/a5a433e089b3b67abd9168aec6c6692f0a841ea2/stm32_gpio_write.cpp) [stm32_gpio_write.cpp](https://gist.github.com/MayaPosch/2e4d761821350867cb05016f129f86c7#file-stm32_gpio_write-cpp) hosted with ❤ by [GitHub](https://github.com)

最后，上述代码片段中的`instance`是对启动时静态创建的`std::vector`中的条目的引用。它为每个外设注册属性:


```
|  | STD::vector<gpio_instance>*GPIO _ instances(){ |
|  | GPIO_instance 实例； |
|  | 静态STD::vector<GPIO _ instance>* instance static =newSTD::vector<GPIO _ instance>(12，instance)； |
|  |  |
|  | # if 定义了 RCC_AHBENR_GPIOAEN &#124;&#124;定义了 RCC_AHB1ENR_GPIOAEN &#124;&#124;定义了 RCC_APB2ENR_IOPAEN |
|  | ((* instance static))[GPIO _ PORT _ A]。regs= GPIOA； |
|  | # endif |
|  |  |
|  | # if 定义了 RCC_AHBENR_GPIOBEN &#124;&#124;定义了 RCC_AHB1ENR_GPIOBEN &#124;&#124;定义了 RCC_APB2ENR_IOPBEN |
|  | ((* instance static))[GPIO _ PORT _ B]。regs= GPIOB； |
|  | # endif |
|  |  |
|  | [..] |
|  |  |
|  | 返回instance static； |
|  | } |
|  |  |
|  | 静态STD::vector<GPIO _ instance>* instance static = GPIO _ instances()； |
```

[view raw](https://gist.github.com/MayaPosch/5128d064d2048d353180dc319a918810/raw/1a12b6a2ae0bc4e85a896b4dbafe870b4abee5ad/stm32_gpio_instances.cpp) [stm32_gpio_instances.cpp](https://gist.github.com/MayaPosch/5128d064d2048d353180dc319a918810#file-stm32_gpio_instances-cpp) hosted with ❤ by [GitHub](https://github.com)

如果外设存在(即在该 MCU 的 CMSIS 头中列出，例如 [STM32F042](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/cpp/core/include/stm32f0/stm32f042x6.h) ，则在`GPIO_instance`结构中创建一个条目，指向其存储器映射寄存器(`regs`)。然后，这些实例可以与其中的任何元信息一起被引用，例如它们是否已经被激活:

```
|  | GPIO _ instance & instance =(* instance static)[port]； |
|  |  |
|  | // 检查端口是否激活，如果没有，尝试激活。 |
|  | 如果(!instance.active) { |
|  | 如果(Rcc::enable port((Rcc port)port)){ |
|  | 实例。主动 = 真实； |
|  | } |
|  | 否则 { |
|  | 返 假； |
|  | } |
|  | } |
```

[view raw](https://gist.github.com/MayaPosch/7139aa853733d12d5fdbb5c7e9ec6419/raw/65a6b114371f34a1692f1de439d4725c0c5d02e4/stm32_gpio_instances_get.cpp) [stm32_gpio_instances_get.cpp](https://gist.github.com/MayaPosch/7139aa853733d12d5fdbb5c7e9ec6419#file-stm32_gpio_instances_get-cpp) hosted with ❤ by [GitHub](https://github.com)

这样做的好处是——如前所述——无论我们寻址哪个外设，都可以使用相同的代码，因为它们在寄存器布局方面完全相同。

## 救援指挥中心(Rescue Control Center)

[RCC 类](https://github.com/MayaPosch/Nodate/blob/master/arch/stm32/cpp/core/src/rcc.cpp)还使用相同的 CMSIS 预处理器定义来跟踪外设是否存在，以防止任何意外。此后，使能外设时钟就变得非常容易:



|  | boolRcc::enable(Rcc 外设){ |
|  | uint 8 _ tperNum =(uint 8 _ t)外设； |
|  | RccPeripheralHandle & ph =(* perHandlesStatic)[perNum]； |
|  |  |
|  | 如果(博士存在 == 假 ) { |
|  | 返 假； |
|  | } |
|  |  |
|  | // 检查当前外设状态。 |
|  | 如果 (ph. 计数 > 0 ) { |
|  | 如果(博士计数 > = handle_max) { |
|  | 返 假； |
|  | } |
|  |  |
|  | // 增加一个处理器计数。 |
|  | ph. 计数++； |
|  | } |
|  | 否则 { |
|  | // 激活外设。 |
|  | ph. 计数=1； |
|  | *(ph .ENR)&#124; =(1<<ph .使能)； |
|  | } |
|  |  |
|  | 返回 真实； |
|  | } |

[view raw](https://gist.github.com/MayaPosch/9443988784d8e31ce2c00a900a3be7a6/raw/9ce91f6f2a6cf5dd9712b3ce75a70a9c4248f350/stm32_rcc_enable.cpp) [stm32_rcc_enable.cpp](https://gist.github.com/MayaPosch/9443988784d8e31ce2c00a900a3be7a6#file-stm32_rcc_enable-cpp) hosted with ❤ by [GitHub](https://github.com)

除了切换相关的位位置(`ph.enable`)，我们还执行引用计数，这样我们就不会在代码的另一部分仍在使用外设时意外禁用它。

## 运行示例

看完上面的材料后，我们应该对“咄咄逼人”的例子在基本层面上是如何运作的有所了解。我们现在可以构建和运行它。如上所述，为此我们需要安装 ARM 工具链和 Nodate 框架。前者可以通过自己喜欢的包管理器(包:arm-none-eabi-gcc)或者 [Arm 网站](https://developer.arm.com/tools-and-software/embedded/arm-compiler/downloads/version-6)获得。Nodate 框架通过 Github 获得，之后必须在一个全局 **NODATE_HOME** 系统变量中指定 Nodate 根文件夹的位置。

完成后，导航到 Nodate 文件夹，并进入`examples/stm32/pushy`文件夹。在这里，打开 [Makefile](https://github.com/MayaPosch/Nodate/blob/master/examples/stm32/pushy/Makefile) 并选择任何电路板预设(目前为蓝色药丸、Nucleo-F042K6、STM32F4-Discovery 或 Nucleo-746ZG)。接下来，打开`src/pushy.cpp`并确保目标板的相应行未被注释。

接下来，在 Makefile 所在的文件夹中，用`make`构建。通过 ST-Link 连接目标板，确保 OpenOCD 已安装，并使用`make flash`闪烁。这应该会将固件映像写入主板。

当按钮连接到指定的引脚和`Vdd`时，按下该按钮将使板上的 LED 灯亮起。这演示了 STM32 GPIO 外设的基本用法，您已经比“blinky”更进了一步。

希望这显示了裸机 STM32 的开发是多么简单。请继续关注更高级的主题，我们会进一步深入这个主题。