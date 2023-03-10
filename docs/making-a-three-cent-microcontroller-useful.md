# 使三分微控制器变得有用

> 原文：<https://hackaday.com/2019/04/26/making-a-three-cent-microcontroller-useful/>

红木 PMS150C 是一个可怕的微控制器。只有六个引脚，只有一千字的闪存，64 字节的 RAM，而且它不做乘法。这个芯片只能写一次代码，IDE 使用的是 8 位 int。[安德斯]得到了一些芯片，并决定用它们做些有用的事情。事实证明，你可以用最少的硬件做很多事情，比如用一个三分微控制器驱动 300 个 RGB LEDs。

有一些工作试图让 T2 为这些芯片做一个开源工具链，但是安德斯决定只使用制造商 IDE 和程序员。然而，如何处理三分微控制器呢？显然是闪光的东西。[Anders]将这个微控制器连接到一条 Neopixels 或 WS2812Bs，但不是通过给每个像素几个字节的 RAM 来驱动它们，而是一次一位地对整个条进行位碰撞。这是一些聪明的代码，即使[Anders]无法将图像发送到由 Neopixels 制成的巨大图形显示器上，这仍然是一个巧妙的技巧。

三美分，几乎没有相关硬件，这是我们见过的最便宜的微控制器。即使是极简的 PIC 和 AVR 部分也在*几十美分*一个部分的量级，仍然只有这三分钱部分的功能。[制造商的页面](http://www.padauk.com.tw/en/product/show.aspx?num=4)有更多关于微控制器本身的细节，包括[的数据表](http://www.padauk.com.tw/upload/doc/PMS15A,PMS150C%20datasheet%20V106_EN_20190327.pdf)，你可以查看下面这个项目的 sizzle reel。

 [https://www.youtube.com/embed/zdhI0kNYR_c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zdhI0kNYR_c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

