# 你口袋里的科学实验室？

> 原文：<https://hackaday.com/2019/01/31/a-science-lab-in-your-pocket/>

由于现在即使是最便宜的手机或电脑也有足够的马力，因此有一种趋势是创建可以做任何事情的仪器，使用合理简单的前端并在主机设备上处理数据。这是一项看似简单的任务，但要做好它却需要付出很多努力。我们最近注意到的一个是[袖珍科学实验室](https://pslab.io/)——一个连接到你的 PC 或 Android 手机的电路板，提供示波器、逻辑分析仪、波形发生器、电源、万用表和一些奇怪的物品，如加速度计、气压计、指南针和勒克斯表。成本大约是 65 美元，所以这不是一个大的投资。但是它能做什么呢？请继续阅读，或者您可以观看下面来自新加坡极客营的视频。

数据手册显示了一个合理的设备，虽然没有什么惊人的。示波器有 4 个通道，但只有 2 个 MSPS，因此假设前端可以处理它，您可能会看到 1 MHz 正弦波。还有一个 12 位电压表，三个不同范围的 12 位电源，一个 4 MHz 4 通道逻辑分析仪，两个正弦波或三角波发生器，4 个 PWM 输出，以及测量电容的能力。最后，还有一个频率计数器，可以达到 16 MHz。

示波器上的 4 个通道是受欢迎的，但低采样率是不受欢迎的。此外，数据手册中没有说明，但这类器件的最大问题之一是不能同时使用主要功能。例如，我们打赌你不能同时使用示波器和逻辑分析仪。

就价格而言，这是一笔不错的交易。但是它真的不是几乎所有虚拟仪器的合适替代品。另一方面，不到 70 美元，它可能值得一试。有一个 [Linux 应用](https://github.com/fossasia/pslab-desktop)，所以这是一个优势。我们喜欢它是完全开源的，所以你可以修复任何你不喜欢的东西。

你可以从 FOSSASIA 通道上的[测光表](https://www.youtube.com/watch?v=-Z3VkB4Rtl0)中看到测井数据。他们也有一个关于[波形发生器](https://www.youtube.com/watch?v=NC2T5kElWbE)的视频。

Analog Discovery 2 看起来更好，但不是开源的，也更贵。它也有更好的规格。当然，你不需要一台个人电脑就能拥有[一台万能仪器](https://hackaday.com/2010/06/04/superprobe/)。

 [https://www.youtube.com/embed/-Z3VkB4Rtl0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-Z3VkB4Rtl0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

