# 进行芯片移植来复活一个死板

> 原文：<https://hackaday.com/2018/10/16/performing-a-chip-transplant-to-resurrect-a-dead-board/>

[Uri Shaked]不小心用 12 V 鳄鱼夹碰到了他 3.3 V 板上的一个 GPIO 引脚，把板烤焦了。听起来熟悉吗？更换一个要花 60 美元，这对他来说可不便宜。此外，他需要它为即将到来的会议，所以时间是至关重要的。他唯一的选择[是尝试修复它](https://medium.com/@urish/back-from-the-dead-how-i-revived-a-fried-espruino-board-cf70bdb008e8)，这最终涉及到一个微妙的芯片移植。

![Removing the shield on the Bluetooth LE board](img/91284cac05cea5f7411722ef2d65b526.png)开发板是 Pixl.js，这是一种 LCD 开发板，采用 nRF52832 SoC，配有 ARM Cortex M4、RAM、flash 和蓝牙 LE。它还预装了 Espruino JavaScript 解释器，当然还有 GPIO 引脚，破坏就是通过这些引脚进行的。

幸运的是，他有良好的直觉，在事件发生后立即感觉到 nRF52832 上方的金属护罩。天气很热。在电路板上施加 3.3 V 电压也加热了芯片，让他确认芯片短路了。他所要做的就是换掉它。

四处挖掘，他在不同的板上发现了另一个 nRF52832。令我们惊讶的是，移植它并让电路板重新启动和运行只花了一个小时，包括编写文档的时间。如果这听起来简单，那只是一个熟练的人让事情看起来简单的方式。它包括大量精细的热风枪工作，一些烙铁显微手术，以及使用 JLink 调试器的持久性。但是我们会把手术的细节和并发症留给他的博客。你可以在下面的视频中看到其中的一个步骤。

毫不奇怪[Uri]能够挖掘出另一个具有相同 nRF52832 芯片的板。这是一款受欢迎的 SoC，被用于[微型袖珍机器人](https://hackaday.com/2018/09/15/the-tiny-pocket-sized-robot-meant-for-hacking/)、[会议徽章](https://hackaday.com/2018/08/29/all-the-badges-of-def-con-26-vol-3/)、[Primo 核心板以及各种其他传感器](https://hackaday.com/2017/01/06/ces17-arduino-unveils-lora-modules-for-the-internet-of-things/)。

 [https://www.youtube.com/embed/J1qZpVMhvFg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/J1qZpVMhvFg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

