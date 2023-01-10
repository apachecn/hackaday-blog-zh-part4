# 简单的 Arduino 构建让您可以密切关注 Pi

> 原文：<https://hackaday.com/2022/03/15/simple-arduino-build-lets-you-keep-an-eye-on-pi/>

你是一个数学迷，需要一个新的桌面玩具吗？那我们有项目给你吗？除了一个 Arduino 和一个七段 LED 模块，[[克里斯蒂亚诺·蒙泰罗]已经组装了一个小工具](https://www.linkedin.com/pulse/happy-%25CF%2580-day-2022-cristiano-monteiro)，它将永远缓慢地通过圆周率的数字……或者直到你厌倦了看它并决定将这些部件用于其他用途。

在硬件方面，我们真的不能夸大这个项目有多简单。一个普通的四位 LED 显示屏连接到一个 Arduino Nano 上，然后插入计算机供电。[Cristiano]在这里使用的是试验板，但你也可以轻松地使用四个母到母跳线将两个器件连接在一起。我们认为，对于任何希望获得 PCB 设计实践经验的人来说，这将是一个非常好的项目。

真正的魔力在于软件，[克里斯蒂亚诺]在麻省理工学院的许可下发布了这个软件。在 ATmega328P 这样一个资源受限的芯片上计算圆周率远非理想，但通过移植由[Xavier Gourdon]和[Pascal Sebah]为他们的论文*开发的 C++算法，在低内存*的情况下计算π的第 n 个十进制数字，他能够完成这项任务，尽管速度很慢。

现在，如果你有稍微好一点的硬件，比如说一对至强处理器和 96 GB 的 RAM，[你可以计算出几万亿位数的圆周率来取乐，](https://hackaday.com/2011/11/28/calculating-pi-to-10-trillion-digits-the-last-number-is-5/)但它看起来不会像这个小家伙眨眼一样酷。

 [https://www.youtube.com/embed/QiNvTxBwYYY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QiNvTxBwYYY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

