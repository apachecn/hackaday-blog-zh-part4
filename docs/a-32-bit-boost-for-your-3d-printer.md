# 为您的 3D 打印机提升 32 位性能

> 原文：<https://hackaday.com/2019/05/10/a-32-bit-boost-for-your-3d-printer/>

这可能不是你想得太多的那种东西，但如果你曾经使用过桌面 3D 打印机，它几乎肯定是由 8 位 CPU 控制的。事实上，通用斜坡控制器本质上只是 Arduino Mega 的电机驱动器屏蔽。我们肯定能在 2019 年做得比这更好吗？

[![](img/294a260e7a5c6cfbf54ceb5cd11aa543.png)](https://hackaday.com/wp-content/uploads/2019/05/3dpboard_detail.jpg) 为了参加今年的 Hackaday 奖，【Robert】正在研究一种 32 位嵌入式替代板，它将[允许 3D 打印机所有者轻松升级他们机器的“大脑”](https://hackaday.io/project/160709-upgrade-your-3d-printer-from-8bit-to-32bit)。当然，市场上已经有一些 32 位控制板，但这些几乎都是高端板，很难改装到旧机器上。不用说，它们也不便宜。

借助该主板，[Robert]希望为 8 位打印机用户创造一条更简单的升级途径。体积小、价格便宜已经是一件大事了，但也许同样重要的是，他的主板运行的是开源的马林固件。Marlin 为大多数 8 位桌面 3D 打印机提供动力(即使它们的所有者不一定意识到这一点)，因此坚持使用它意味着用户不应该仅仅因为他们升级了控制器就必须改变他们的软件配置或工作流程。

该板由 72 MHz STM32F103 芯片供电，并使用最先进的 Trinamic TMC2208 步进驱动器来实现近乎静音的操作。该板有一个自动冷却风扇来帮助保持凉爽，并有一个 XT60 电源连接器，它甚至应该是相对容易的[带着合适的结实的 RC 电池](https://hackaday.com/2019/01/21/building-a-3d-printer-that-goes-where-you-do/)去旅行。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)