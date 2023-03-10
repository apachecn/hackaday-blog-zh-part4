# 制作自己的老式 LED 显示屏

> 原文：<https://hackaday.com/2019/05/31/make-your-own-old-school-led-displays/>

我们生活在这样一个时代，各种各样的显示器都很便宜，而且很容易买到。在网上花几美元就能买到一个两行字母数字的液晶显示器，一个图形有机发光二极管屏幕，或者其他各种各样的选择。然而，几年前，人们凑合着使用小型单片 LED 设备。[【sjm 4306】想再造一个类似的东西，开始着手工作(Youtube 链接，嵌入下方)](https://www.youtube.com/watch?v=B2iPQR-sXc4)。

最终的器件使用 0603 尺寸的 SMD LEDs，焊接在一个微型 PCB 上。每个数字使用 20 个 led，可以显示数字 0-9 和字母 A-f。led 的布局模式类似于多年前惠普的设计。与更经典的 7 段设计相比，这种布局让数字看起来更舒适。有几种方法可以使器件尽可能紧凑，例如在 LED 焊盘上设置过孔。这通常是一种糟糕的设计技术，但它有助于节省宝贵的空间。

[sjm4306]开发了一个试验板模型，以及一个更高级的版本，其后部有一个焊盘，可以直接安装 PIC16F88 微控制器。我们期待看到这些模块被进一步开发，并且可以想象它们会在各种项目中被证明是有用的。

作为参考，看看这些苏联时代的 7 段显示器。休息后的视频。

 [https://www.youtube.com/embed/B2iPQR-sXc4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B2iPQR-sXc4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

