# 配有真正涡轮增压器的老式电脑

> 原文：<https://hackaday.com/2021/11/03/vintage-computers-with-a-real-turbo/>

在前几个世纪，将程序的运行与计算机的时钟速度联系起来是一种常见的做法。随着计算机越来越快，与较慢时钟速度相关的程序有时会运行困难。为了暂时解决这个问题，20 世纪 90 年代初的一些计算机包含了一个“涡轮”按钮，它实际上降低了计算机的时钟速度，以帮助旧软件运行，而不会以通常不可预测的方式中断。[Ted Fried]决定彻底改变这个想法，[在旧电脑的硬件中内置一个涡轮按钮](https://microcorelabs.wordpress.com/2021/09/29/ultimate-apple-ii-accelerator-the-mcl65-fast/)，这将大大提高这些电脑的执行速度，而不会造成软件混乱。

为此，他在 Teensys (Teensies？)，但它们被配置为 Apple II、VIC-20 和 Commodore 64 等几台老式计算机的物理 CPU 的替代产品，而不是整个系统的仿真器。它可以配置为在周期精确模式下运行，使其与计算机的原始硬件基本相同，或者可以设置为加速模式，以利用 Teensy 4.1 的 800 MHz 处理器，该处理器比原始硬件快几个数量级。这允许(大部分)原始硬件仍然被使用，同时以更快的速度运行程序，而不需要担心由于时钟速度增加而导致的任何编程中断。

下面的视频演示了[Ted]在 Apple II 上运行的创作，但他有几个用于其他复古计算机的其他内核。这当然是从这些古董机器中挤出更多计算能力的独特方式。一些 Apple II 电脑有 4 MHz 的时钟，按照现代标准看起来慢得令人难以置信，所以按照当时的标准，800 MHz 的 Teensy 应该被认为是神奇的，但信不信由你，对于一些应用程序来说，实际上有必要反其道而行之，将这台电脑的速度降低到 1 MHz。

 [https://www.youtube.com/embed/lrNijAa3qNU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lrNijAa3qNU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

