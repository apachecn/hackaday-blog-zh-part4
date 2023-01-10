# 144 个 7 段显示屏组合成一个强大的时钟

> 原文：<https://hackaday.com/2020/03/05/144-7-segment-displays-combine-to-form-a-mighty-clock/>

你用 144 个 7 段显示器做什么？如果你是[Frugha]，你就把它们放在一起[创造一个史诗时钟](https://hackaday.io/project/169632)。每个显示屏有 8 个独立的发光二极管— 7 段和一个小数点。把这些放在一起，你就有 1152 个独立的发光二极管可以控制。这带来了一个问题，因为[Frugha]想要用一个 Arduino Nano 来控制时钟。即使是 charlieplexing 也不会给你那么多 I/O 线。

解决方案是一个叫做 MAX7219 的漂亮的小芯片。7219 支持 SPI，可以控制 64 个独立的 led。[Frugha]在时钟中使用了 18 个，使他能够完全控制所有的 led。这相当令人印象深刻，考虑到我们看到的上一个 [matrix 7 段显示器需要 48 个 arduino](https://hackaday.com/2013/11/21/7-segment-display-matrix-visualizes-more-than-numbers/)！

另一个问题是内存——1152“像素”会很快超过 ATmega328 的 2KB RAM。不过这是一个时钟——这意味着只有数字 0-9 和一个冒号。[Frugha]挑选了一种漂亮的字体，并为每个数字手工编写了查找表。查找表存储在 ROM 中，节省了 Arduino 上宝贵的 RAM。

如果不准确，一个钟就没有任何用处。一个微型 RTC 提供电池供电的时间数据。[Frugha]在定制的 PCB 上用一个整洁的布局包装了所有东西。当然，你可以把它放在一个盒子里，但是我们认为这个疯狂的钟值得开放——所以你可以看到它所有的荣耀。