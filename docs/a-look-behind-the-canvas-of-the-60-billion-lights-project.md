# “600 亿盏灯”项目背后的一瞥

> 原文：<https://hackaday.com/2020/06/08/a-look-behind-the-canvas-of-the-60-billion-lights-project/>

今年五月，[Erich Styger]向世界展示了他的项目“600 亿盏灯”。现在他公布了这件令人印象深刻的艺术品制作的最新进展。简单回顾一下，[“600 亿盏灯”](https://mcuoneclipse.com/2020/05/24/60-billion-lights-2400-rgb-leds-and-120-stepper-motors-hiding-behind-canvas-art/)是一件画布艺术作品，其中集成了 60 个双轴步进电机。每个步进电机有 40 个 24 位 RGB LEDs，在整个画布上总共有 600 亿个位置和灯光组合。

[![](img/9f339854f1f70384a2e2a39d0de03b50.png)](https://hackaday.com/wp-content/uploads/2020/06/laser-cut-acrylic_thumbnail.png) 通过双轴步进电机，人们可以控制组成一个单元的 40 个凹陷内的激光切割丙烯酸棒的位置。每个单元的 WS2812B LEDs 位于内侧边缘。

正如嵌入的视频(休息后)所示，它可以用来创建各种各样的效果。整个系统由 15 块控制板驱动，这些控制板在通过 [RS-485](https://en.wikipedia.org/wiki/RS-485) 连接的[恩智浦 LPC845](https://www.nxp.com/products/processors-and-microcontrollers/arm-microcontrollers/general-purpose-mcus/lpc800-cortex-m0-plus-/low-cost-microcontrollers-mcus-based-on-arm-cortex-m0-plus-cores:LPC84X) (Cortex-M0+)上运行 FreeRTOS。

在“制作”视频(休息后嵌入)和文章中，显示了单个组件的更多细节，包括双轴步进电机、步进电机印刷电路板、LED 环形印刷电路板以及无数的施工、喷漆和装配图像。

如果最初的文章给人的印象是这是一个简单的项目，这是幕后的样子，给人一个全面的良好印象。从无数的 PCB、控制板、布线、编程到组装和测试。更不用说画布本身的绘画，这是一个原创作品。

 [https://www.youtube.com/embed/rm9YJRw8Cro?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rm9YJRw8Cro?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/XZptepVOI2g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XZptepVOI2g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

