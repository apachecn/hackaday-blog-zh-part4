# 工具为您编写 PWM 代码

> 原文：<https://hackaday.com/2020/02/06/tool-writes-your-pwm-code-for-you/>

电脑的好处是它们替你工作，对吗？如果你是一名程序员，这似乎并不总是正确的说法。[Runtimemicro]给出了答案，至少如果你正在为 Arduino 编写 PWM 代码。他们的[免费应用](https://runtimemicro.com/Projects/WYSIWYG-Arduino-PWM-Code-Generator)让你设置一些参数，直观地看到结果，然后为你生成代码。您可以在下面看到该工具运行的视频。

根据他们的网站，该工具适用于 Arduino Nano、Uno 或 Mega2560 上的定时器 1 至 5。这款应用似乎可以在 Windows 上运行，但在 Wine 下运行在其他平台上似乎不会有任何问题。

只有几个输入:时钟速度，你想使用哪个定时器，以及模式。您还必须以 Hz 为单位指定频率，或者以毫秒为单位指定周期。您还可以选择几个选项，包括是否希望生成中断代码。

一旦计时器出现在图形显示中，您可以调整一些滑块来获得您想要的精确 PWM 占空比。当然，您也可以跳过 PWM 代码，直接使用定时器中断进行计时。

这并不是说定时器代码或 PWM 没有工具就无法工作。不过话说回来，你并不真的需要汇编器或编译器——它只是让事情变得更简单。尽管如此，还是有一些细微的差别。如果你想深入研究生成的代码，你可能会发现[【杰克的】视频很有趣](https://hackaday.com/2011/10/27/video-pwm-on-the-atmega328p/)。

 [https://www.youtube.com/embed/Slhe3Ud6YBo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Slhe3Ud6YBo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

