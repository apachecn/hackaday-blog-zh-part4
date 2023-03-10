# 查看试验板上的二进制代码

> 原文：<https://hackaday.com/2018/09/08/see-binary-on-your-breadboard/>

当您调试具有 ESP32、Raspberry Pi 或 Arduino 的电路板时，很容易点击一个小型 LCD 显示器或通过 WiFi 连接来查看问题所在。至少，孩子们是这么做的。但是如果你是守旧派或者你没有那种满是粉刺和类固醇的董事会呢？电阻器和 LED 通常就足够了。给 LED 供电是一回事，不给它供电是另一回事。多了七个发光二极管，你甚至可以用二进制显示 0-255。

[米格尔]显然属于后一种阵营。为了让 LED 的调试变得容易，他想出了一个带电阻器的 8 LED 电路板。他甚至还包括了你制作自己所需的 Gerber 文件。一排引脚全部连接在一起，而另一排没有。所以，你是使用共阴极还是共阳极取决于你焊接 led 时的方向。你可能已经准备好了每种类型的一块板子。

但是我们在骗谁呢？这只是在试验板上的普通乐趣。向朋友展示你的原型小玩意，你知道他们会被角落里的小二进制计数器吸引，它会发出 42 的脉冲或倒计时，直到它开始闪烁 255。

冒着功能过于丰富的风险，你可以[为二进制键盘添加两个键](https://hackaday.com/2017/04/17/this-binary-keyboard-is-for-ascii-purists/)或者[添加更多的 led 来显示 32 位二进制 Unix 纪元时间](https://hackaday.com/2013/08/14/unreadable-binary-epoch-clock-is-unreadable/)，然后看看还有多久你的朋友们才能弄明白。

 [https://www.youtube.com/embed/P_pVd3iIPwU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/P_pVd3iIPwU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

