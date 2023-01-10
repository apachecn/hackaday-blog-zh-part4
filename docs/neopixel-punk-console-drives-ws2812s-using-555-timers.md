# NeoPixel Punk 控制台使用 555 定时器驱动 WS2812s

> 原文：<https://hackaday.com/2022/01/01/neopixel-punk-console-drives-ws2812s-using-555-timers/>

NeoPixels 是一种具有可单独寻址像素的 LED 灯条，是复杂灯光效果创作者的最爱。它们因其多功能性和易于菊花链连接而广受欢迎。尽管由于严格的信号时序限制，驱动这些小 led 的协议可能很难实现。

然而，[Adrian Studer]证明了驱动基于 WS2812 的 LED 灯条(如 NeoPixel 系列)不一定需要手工优化汇编代码。事实上，它根本不需要任何代码。他建造了 NeoPixel Punk 控制台，这是一种甚至不使用微控制器就能创造灯光秀的设备。只有少数 555 定时器和一些 74HC 系列逻辑一起工作，以产生具有近似正确定时的脉冲。

操作该设备就像调整几个电位计一样简单，就像它的同名物[雅达利朋克控制台](https://hackaday.com/2015/09/17/the-ubiquitous-atari-punk-console/)一样。不过这是一个相当随机的过程，你可能无法重新创建一个你喜欢的模式。此外，尽管[Adrian]计划制造一种改进版本，分别驱动红色、绿色和蓝色子像素，但 led 大多以原色全功率发光。但事实上，所有这一切都是由一堆 555 定时器实现的，这使得它无论从哪个标准来看都是一个相当令人印象深刻的黑客。

我们已经看到了许多驱动 NeoPixels 或类似的基于 WS2812 的 LED 灯条的方法，尽管它们都使用某种微处理器；你可以启动经典的 6502(T1)，在 pic 32(T3)上使用(T2)SPI 和 DMA，或者只需插入(T4)一个单臂 Cortex M0+(T5)。

 [https://www.youtube.com/embed/qSbU0WfGY8Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qSbU0WfGY8Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

