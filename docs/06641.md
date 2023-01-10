# 从 TFT 显示器窃取微控制器的 RAM

> 原文：<https://hackaday.com/2020/05/21/stealing-ram-for-a-microcontroller-from-a-tft-display/>

记性好的个人电脑用户会回想起一兆字节障碍是个大问题的日子，以及用来减轻它的各种扩展和扩充内存的技巧。其中之一是安装一个驱动程序，当显示器处于 DOS 文本模式时，该驱动程序将多余的显卡内存映射为系统内存，当我们读到[Frank D]的[微控制器实现康威的生命游戏](https://ioprog.com/2020/05/19/breadboard-games-2020/)时，我们想到的就是这个。

组件是他必须手；一块 STM32F030F4P6 和一块 RM68130 176 × 220 TFT 板。STM 并不是最强大的芯片，只有 16 kB 的闪存和 4 kB 的 RAM。显示器有足够的板载内存来支持 18 位颜色信息，但当它在八色模式下运行时，它只使用其中的三种。剩余的 15 位因此可用于其他目的，虽然读取它们的神秘格式需要一些理解，但它们可以用于为微控制器提供非常有用的额外 38720 字节 RAM，就像以前的 DOS PC 显卡一样。有趣的是，同样的技术应该适用于其他类似的显示器。

尽管这绝不是一项新技术，但我们不记得以前在这样的微控制器项目中见过它。我们给你带来了许多生命的游戏，以及今年早些时候约翰·康威的去世。

 [https://www.youtube.com/embed/XIE2ECZmJnc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XIE2ECZmJnc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

