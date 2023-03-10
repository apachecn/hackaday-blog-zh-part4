# FreeRTOS 和 ChibiOS 入门

> 原文：<https://hackaday.com/2021/03/18/getting-started-with-freertos-and-chibios/>

如果操作系统不是如此有用，我们就不会在我们的每一个桌面系统上运行它们。同样，嵌入式操作系统提供与这些桌面操作系统相似的功能，同时针对更专业的市场。其中一些是桌面操作系统的改编版本(如 Yocto Linux)，而另一些则是为嵌入式应用从头开始构建的，如 VxWorks 和 QNX。然而，这些操作系统中很少能在微控制器(MCU)上运行。当您需要在 8 位 AVR 或 32 位 Cortex-M MCU 上运行操作系统时，您需要更小的系统。

类似 ChibiOS(日语中“Chibi”的意思是“小”)或 FreeRTOS(这里没有原创性)。也许更准确地说，FreeRTOS 可以被概括为一个针对低功耗系统的多线程框架，而 ChibiOS 则更像是一个全功能的操作系统，包括一个硬件抽象层(HAL)和其他细节。

在本文中，我们将更深入地了解这两个操作系统，看看它们带来了什么好处。

## 基本功能集

[FreeRTOS](https://en.wikipedia.org/wiki/FreeRTOS) 支持几十个微控制器平台，最引人注目的可能是 AVR、x86 和 ARM (Cortex-M & Cortex-A)。相比之下， [ChibiOS/RT](https://en.wikipedia.org/wiki/ChibiOS/RT) 可能在更少的平台上运行，但带有一个 HAL，它抽象出了包括 I2C、CAN、ADC、RTC、SPI 和 USB 外设在内的硬件设备。它们都提供了具有优先级和多线程原语的[抢占式](https://en.wikipedia.org/wiki/Preemption_(computing))多任务调度程序，包括互斥、条件变量和信号量。

这种比较的必然结果似乎是 FreeRTOS 适合基本的多线程特性，而 ChibiOS/RT 通过其 HAL 提供了更全面的方法。HAL 的出现也意味着理论上可以针对 ChibiOS/RT，为不同的 MCU 平台重新编译相同的代码。对于 FreeRTOS 来说，人们仍然需要使用另一个框架来使用硬件外设，无论是 CMSIS、ST 的 HAL 还是其他什么，这都会降低可移植性。

在接下来的部分中，我们将通过这两个操作系统的一个基本例子，来更深入地理解使用它们进行开发是什么样的。

## with CMSIS 公司的 FreeRTOS

[![](img/7726575a8479043e7423a4b96bdc4519.png)](https://hackaday.com/wp-content/uploads/2021/01/screenshot_stm32f746_http_server_cropped.jpg)

A HTML page, served from an STM32F746ZG MCU.

对于如何使用 FreeRTOS 的简单示例，ST 为 Nucleo-746ZG STM32 开发板开发的 [HTTP 服务器示例](https://github.com/STMicroelectronics/STM32CubeF7/tree/master/Projects/STM32F746ZG-Nucleo/Applications/LwIP/LwIP_HTTP_Server_Netconn_RTOS)是一个很好的开始。我还[制作了一个包含所有依赖项的独立版本](https://github.com/MayaPosch/FreeRTOS_HTTP_server)和一个 Makefile，用于与 [Arm Cortex-M GCC 工具链](https://developer.arm.com/tools-and-software/embedded/arm-compiler/downloads/version-6)一起使用。

这个示例项目演示了如何结合 CMSIS-RTOS API、FreeRTOS 和 LwIP 网络堆栈来创建一个基于 Netconn 的 HTTP 服务器，该服务器可以提供文档和图像服务。LwIP 的 Netconn API 是一个比 raw API 更高级的 API，这使它成为在联网方面没有特殊需求的人的首选。

演示项目的入口点在`Core/Src/Main.cpp`中。它的主要目的是设置固件:配置外设和时钟，然后初始化第一个线程。这里我们看到的不是正在使用的[自由操作系统线程](https://www.freertos.org/taskandcr.html)(任务)的语法，而是[CMS is-RTOS](https://arm-software.github.io/CMSIS_5/RTOS/html/group__CMSIS__RTOS__ThreadMgmt.html#gac59b5713cb083702dce759c73fd90dff)的语法，例如:

```

osThreadDef(Start, StartThread, osPriorityNormal, 0, configMINIMAL_STACK_SIZE * 5);
osThreadCreate (osThread(Start), NULL);

static void StartThread(void const * argument)
{
    /* .. */ 
}

```

CMSIS-RTOS 是 *Cortex 微控制器软件接口标准*的一部分，简称 [CMSIS](https://developer.arm.com/tools-and-software/embedded/cmsis) 。它是基于 Arm Cortex 的 MCU 的独立于供应商的硬件抽象层(HAL)。在嵌入式实时操作系统的情况下，CMSIS 提供了 CMSIS-RTOS 规范，该规范允许为通用 RTOS API 编写软件，从而使软件可跨 Cortex-M(和 Cortex-A)移植。然后，每个受支持的 RTOS 提供一个 CMSIS-RTOS 实现来映射这两组 API 调用。

在这个例子中，我们在 FreeRTOS 上使用更基本的 [CMSIS-RTOS v1](https://arm-software.github.io/CMSIS_5/RTOS/html/index.html) API。对于支持 ARMv8 以及多核和 Cortex-A 的新型 MCU 来说， [RTOS v2](https://arm-software.github.io/CMSIS_5/RTOS2/html/index.html) 接口是更好的匹配。FreeRTOS 也支持 RTOS v2 接口，在`Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS_V2`下可以找到相关的必要文件，就在 RTOS v1 的文件夹旁边。

在前面的代码片段中，我们看到了如何创建一个新线程。然而，当我们创建启动线程时，还没有调度程序在运行。我们从调用`osKernelStart()`开始。此后，调度并执行`startThread`函数中的代码。毫不奇怪，这个函数启动了构成 HTTP 服务器的主线程:

```

static void StartThread(void const * argument)
{ 
  /* Create tcp_ip stack thread */
  tcpip_init(NULL, NULL);

  /* Initialize the LwIP stack */
  Netif_Config();

  /* Initialize webserver demo */
  http_server_netconn_init();

  /* Notify user about the network interface config */
  User_notification(&gnetif);

#ifdef USE_DHCP
  /* Start DHCPClient */
  osThreadDef(DHCP, DHCP_thread, osPriorityBelowNormal, 0, configMINIMAL_STACK_SIZE * 2);
  osThreadCreate (osThread(DHCP), &gnetif);
#endif

  for( ;; )
  {
    /* Delete the Init Thread */ 
    osThreadTerminate(NULL);
  }
}

```

我们首先调用`[tcpip_init()](https://www.nongnu.org/lwip/2_1_x/group__lwip__os.html#gae510f195171bed8499ae94e264a92717)`，它创建了 LwIP TCP/IP 处理线程(tcpip_thread)。`Netif_Config()`是我们代码中的网络接口配置函数。它调用 [LwIP NETIF 函数](https://www.nongnu.org/lwip/2_0_x/group__netif.html) `netif_add()`和`netif_default()`来添加并设置我们的新网络接口为默认接口。有了这个，我们就有了充分的

`http_server_netconn_init()`功能位于`httpserver-netconn.c`中。它创建了一个名为 HTTP 的新线程，该线程运行 http_server_netconn_thread 中的代码。这将在端口 80 上设置服务器套接字，并等待新的传入连接。然后由`http_server_serve()`函数处理，这是一个简单的 if/else 块，用于解析 HTTP 请求，或者提供静态文件内容(硬编码在字节数组中)，或者显示由`DynWebPage()`生成的动态信息(对于一个 */STM32F7xxTASKS.html* 请求):

```

void DynWebPage(struct netconn *conn)
{
  portCHAR PAGE_BODY[512];
  portCHAR pagehits[10] = {0};

  memset(PAGE_BODY, 0,512);

  /* Update the hit count */
  nPageHits++;
  sprintf(pagehits, "%d", (int)nPageHits);
  strcat(PAGE_BODY, pagehits);
  strcat((char *)PAGE_BODY, "

<pre>
Name          State  Priority  Stack   Num" );
  strcat((char *)PAGE_BODY, "
---------------------------------------------
");

  /* The list of tasks and their status */
  osThreadList((unsigned char *)(PAGE_BODY + strlen(PAGE_BODY)));
  strcat((char *)PAGE_BODY, "

---------------------------------------------");
  strcat((char *)PAGE_BODY, "
B : Blocked, R : Ready, D : Deleted, S : Suspended
");

  /* Send the dynamically generated page */
  netconn_write(conn, PAGE_START, strlen((char*)PAGE_START), NETCONN_COPY);
  netconn_write(conn, PAGE_BODY, strlen(PAGE_BODY), NETCONN_COPY);
}

```

这个函数有趣的地方在于，它提供了对活动线程的洞察，这是从对`[osThreadList()](https://github.com/STMicroelectronics/STM32CubeF0/blob/4390ff6bfb693104cf97192f98c3dc9e3a7c296a/Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS/cmsis_os.c#L1541)`的调用中获得的。尽管不是 v1 CMSIS-RTOS API 的官方部分，但它确实提供了有用的功能。然而，这确实表明，尽管 CMSIS-RTOS HAL 是有用的，但它是不完美的，并且可能默认不覆盖更奇特的用例，或者不能从底层操作系统暴露 API。

[![](img/6978686cdc2ae9db97cc3ab7267c4e05.png)](https://hackaday.com/wp-content/uploads/2021/01/NUCLEO-F746ZG.jpg)

A Nucleo-F746ZG development board.

除此之外，其余的`StartThread()`功能并不令人惊讶:`User_notification()`功能(可以在`app_ethernet.c`中找到)设置 Nucleo 开发板上的 led 来指示连接状态。如果我们已经启用了 DHCP 支持，那么也会为此创建一个线程，使用来自同一源文件的`DHCP_thread()`。DHCP 线程尝试使用 LwIP 中的 DHCP 功能获取 IP 地址，并为我们之前创建的接口设置该地址。

此时，我们可以编译项目了。假设我们已经通过 [Arm 下载页面](https://developer.arm.com/tools-and-software/embedded/arm-compiler/downloads/version-6)或者通过我们操作系统的包管理器获得了 *arm-none-eabi* GCC 工具链，这样编译器就在系统路径上，编译基于 Makefile 的项目可以通过简单调用`make`来完成。刷新到 Nucleo-746ZG 开发板需要安装 OpenOCD，之后连接开发板的简单`make flash`就足够了。

## 赤壁:也许没那么小

[![](img/fbd67fd1f3dba75e4f6405ca7b13e02c.png)](https://hackaday.com/wp-content/uploads/2021/01/Development-system-diagram.png)

Developing with ChibiStudio.

正如前面提到的，ChibiOS(讽刺的是)在特性集方面比 FreeRTOS 大得多。当简单地开始一个新的 ChibiOS 项目时，这一点也变得很明显。正如我们之前看到的，FreeRTOS 可以轻松地成为像 CMSIS-RTOS 这样的 HAL 中的 RTOS，而 ChibiOS 有很多 API 没有涵盖的功能。出于这个原因，ChibiOS 项目有自己的(基于 Eclipse 的)IDE，其形式为 [ChibiStudio](http://www.chibios.org/dokuwiki/doku.php?id=chibios:products:chibistudio:start) ，预装了演示项目。

在 Play Embedded 这个网站上，可以找到大量关于 ChibiOS 的教程和文章，比如这篇[介绍文章](https://www.playembedded.org/blog/developing-stm32-chibistudio/)，里面也涵盖了 ChibiStudio 入门。ChibiOS 的复杂性也体现在[配置文件](https://www.playembedded.org/blog/demos-chibios-stm32/)中，其中包括:

*   `chconf.h`，用于配置内核选项。
*   `halconf.h`，用于配置 HAL。
*   `mcuconf.h`，包含与作为目标的特定 MCU 相关的信息。

STM32F042K6 MCU 的 [ChibiOS 下载](https://osdn.net/projects/chibios/releases/)包中提供的“Blinky”示例项目(在 ST Nucleo-F042K6 板上找到)给出了 ChibiOS 项目的大致情况。这里需要注意的是 ChibiOS/HAL 模块的使用，它允许使用 UART2 外设，使用 ChibiOS 的串行驱动程序。

将代码重定向到另一个 MCU 应该是更新配置文件和重新编译的事情，尽管人们认为这应该通过 IDE 来完成，而不是手动完成。粗略地看，与其他 ide 的集成似乎也不是一件事。这可能意味着变得非常熟悉 Doxygen 生成的[文档](http://www.chibios.org/dokuwiki/doku.php?id=chibios:documentation:start)和其他信息。

与此同时，ChibiOS 确实支持 CMSIS-RTOS，并且还提供了两种不同的内核:RT(实时)内核和 NIL，NIL 基本上只是试图在代码大小方面尽可能小。如果他们的基准可信，这种权衡似乎不会对性能产生太大影响，这使得它成为一个新的嵌入式(RT)OS 项目的有趣选择。

## 包扎

在本文中，我们了解了在决定使用 FreeRTOS 还是 ChibiOS 进行开发时会遇到的一些问题。虽然两者都有各自的长处和短处，但其中一个应该注意的要点是，归根结底，它们是两种非常不同的动物。包括它们提供的功能和它们针对的需求。

如果你已经使用了 CMSIS，那么插入 FreeRTOS 是简单而直接的，允许你使用其他 CMSIS 目标代码，如果有任何改变的话，也很少。另一方面，ChibiOS 更像是它自己的东西，这不一定是负面的。也许最有帮助的是将 FreeRTOS 视为一个有用的模块，可以将其附加到 CMSIS 和其他框架上以添加多线程支持，而 ChibiOS 更类似于 [NuttX](https://en.wikipedia.org/wiki/NuttX) 和[泽法](https://en.wikipedia.org/wiki/Zephyr_(operating_system))，作为满足您所有需求的一站式解决方案。