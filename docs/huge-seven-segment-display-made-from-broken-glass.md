# 由碎玻璃制成的巨大七段显示器

> 原文：<https://hackaday.com/2020/02/10/huge-seven-segment-display-made-from-broken-glass/>

作为几十年来消费设备的主要产品，七段显示器可以说是最容易识别的电子组件之一。因此，毫不奇怪，我们自己的项目很容易获得廉价的资源。但这并不意味着没有个人解读的空间。

[MacCraiger]想要建造一个具有经典七段 LED 外观的挂钟，[他的想法只是让它的*比一般的*](https://github.com/craigfoo/glass_clock)稍大一点。有了 RGB LED 条代替单个 LED，在技术层面上扩大这个概念真的不是问题；棘手的部分是扩散这么多的发光二极管，并实现真正的七段显示器的有序外观。

[![](img/1ff9abeb064f502b98a3569d32192c29.png)](https://hackaday.com/wp-content/uploads/2020/02/glassclock_detail.jpg) 所有这些完美地从一张胶合板上切割下来的片段都是由 CNC 路由器提供的。一旦矩形被切下，[MacCraiger]必须用某种东西填充它们，这种东西可以软化安装在它们后面的 led 发出的光。他决定把一堆玻璃瓶分成小块，把它们放在碎片里，然后用一层透明的环氧树脂把它们密封起来。最终的外观是独一无二的，就好像这些部分是冰块一样。

乍一看，使用 Raspberry Pi Zero 来控制 LED 灯条似乎有些过分，但事实证明，[MacCraiger]实际上增加了相当多的额外功能。纯粹主义者可能会说，它仍然可以用 ESP8266 来完成，但是能够在您的时钟内的 Linux 计算机上抛出一些 Python 脚本肯定有其吸引力。

最大的特点是与亚马逊的 Alexa 的互操作性。一旦他告诉数字家庭助理设置闹钟，时钟将切换到倒计时显示，随着计时器接近零，数字会改变颜色。他还写了一些代码，随着月份的进展，数字的颜色慢慢向红色移动，这是一种很好的方式，可以一眼看出你离月底的最后期限有多近。

最近，我们看到了定制多段显示器的热潮。就在上个月，我们看到了[一个时钟，它使用了一些令人难以置信的 25 段 LED 显示屏](https://hackaday.com/2020/01/28/clock-uses-custom-led-displays-to-keep-myst-time/)，并在环氧树脂填充的扩散器上完成了自己独特的外观。

 [https://www.youtube.com/embed/m1vyYFlk2MA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/m1vyYFlk2MA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

