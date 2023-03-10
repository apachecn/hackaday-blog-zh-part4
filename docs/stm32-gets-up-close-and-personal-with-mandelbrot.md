# STM32 近距离接触 Mandelbrot

> 原文：<https://hackaday.com/2020/10/25/stm32-gets-up-close-and-personal-with-mandelbrot/>

Mandelbrot 集是一个奇怪的数学怪物，虽然它本身很有趣，但也是一个对各种类型的计算机进行基准测试的有用工具。它在放大和缩小功能时的持续计算要求，加上它可以无限缩放的事实，意味着它需要一些高质量的硬件和软件才能正确显示。[]than assis]已经将这作为他的一个宠物项目，在许多不同的硬件平台上以不同的方式运行 Mandelbrot 集合可视化。

这个特别的是基于一个叫做 Blue Pill 的 STM32 板，[Thanassis]选择它是因为他还没有在微控制器上做过连续的 Mandelbrot 变焦。显示器由一个微小的 16K IPS 彩色屏幕处理，由于 STM 只有 20 kB 可用，为了获得流畅的视频输出，必须使用一些聪明的内存技巧。在保持连续缩放功能的同时，整数乘法在这么小的平台上也很棘手，所以它仅限于定点乘法。

即使有平台的限制，他仍然能够用这个实现接近两位数的 FPS 速率。如果你想在 STM 平台上玩这样的图形，[Thanassis]已经在他的 GitHub 页面上发布了所有源代码，但是如果你想看到更多 Mandelbrot 操作，你可以查看他的一个旧项目[，他在 FPGA](https://hackaday.com/2018/12/09/fpga-used-vhdl-for-fractals/) 上构建了一个类似的项目。

 [https://www.youtube.com/embed/5875JOnFDLg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5875JOnFDLg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

