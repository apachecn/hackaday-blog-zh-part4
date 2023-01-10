# 皮科米给你的皮科米一个豪华的基本

> 原文：<https://hackaday.com/2021/11/24/picomite-gives-your-pico-a-basic-with-all-the-features/>

是什么让开发微控制器项目变得快速而简单？在我们的列表中，最重要的是一个交互式外壳和处理所有低级外围设备的综合库。你认为我们在说微型 Python 吗？今天不行！MMBasic 刚刚被移植到 Raspberry Pi Pico 开发板上，它已经*了所有的*电池。

为了让你体验一下，它内置了对 SD 卡、各种显示器、触摸屏、实时时钟、红外遥控器、众多传感器的支持，当然还有 WS2812 LED 灯条。因为所有这些都被嵌入到 BASIC 中，所以编写使用这些外设的代码非常简单。

现在，有基本的和基本的。这是一个现代的 BASIC:它有循环、函数、数组、浮点和一个内置的全屏编辑器。你通过 UART 连接到 Pico，然后你就可以参加比赛了。如果你身边有一台微型相机，闪一下试试吧。或者，如果您想了解内部情况，可以查看一下 GitHub 库。

这是 BASIC 的一个端口，用在 [Maximite](https://geoffg.net/maximite.html) 虚拟反计算机平台上，这意味着有许多工作示例可供你借鉴，[甚至还有论坛](http://www.thebackshed.com/forum/ViewTopic.php?FID=16&TID=14232)。再加上非常棒的[用户手册和教程](https://geoffg.net/Downloads/picomite/PicoMite_User_Manual.pdf) (PDF)，你就拥有了一个完美的周末下午。

认为 MicroPython 杀了 BASIC？再想想。BASIC 足够小，它可以在 Python 不能运行的地方运行，但这当然是一种更少的体验。相比之下，MMBasic 看起来好像拥有所有的浇头。整个玉米卷饼。就像是基本豪华版。