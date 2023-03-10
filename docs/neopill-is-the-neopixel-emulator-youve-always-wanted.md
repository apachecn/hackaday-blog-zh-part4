# 尼奥比尔是你一直想要的尼奥像素模拟器

> 原文：<https://hackaday.com/2021/05/26/neopill-is-the-neopixel-emulator-youve-always-wanted/>

NeoPixels 和其他可寻址 LED 串是一项技术，使充满活力、发光的 LED 项目变得人人可及。当然，在实际设置 LED 灯串之前，能够在软件中模拟您的新 glowy 项目是很好的。Randy Elwin 的 NeoPill 模拟器可以帮上忙！

NeoPill 由一个 STM32F103 开发板组成，只需将 NeoPixel 数据线连接到开发板即可。然后，微控制器利用板载定时器和 SPI 硬件对数据进行解码。这些数据然后通过板载 USB 串行连接传递到 PC，由定制的 Python 应用程序解码。该应用程序获取数据并在屏幕上显示像素，因此您可以在连接单个真正的 LED 之前验证它们是否按预期运行。

这是一个很好的工具，花费很少，但工作做得很好。它甚至可以与电路中的 led 一起使用，以验证问题是否与数据输出或硬件本身有关。[Randy]演示了同时处理多达 256 个 led 灯串的软件；我们很想看看它在断裂前能被推多远。Github 上为那些渴望拥有自己的 NeoPill 的人提供了代码。

[它不是唯一的 NeoPixel 模拟器](https://hackaday.com/2020/04/04/neopixel-matrix-simulation-lets-you-virtually-groove-to-the-lights/)，但它是我们见过的第一个可以用来调试来自真实硬件的实际信号的模拟器，这是一个非常有用的工具。休息后的视频。

 [https://www.youtube.com/embed/Eu9OnIIItRc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Eu9OnIIItRc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

