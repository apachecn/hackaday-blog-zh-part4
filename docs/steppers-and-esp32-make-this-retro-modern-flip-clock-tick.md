# 步进器和 ESP32 使这个复古现代翻转时钟滴答作响

> 原文：<https://hackaday.com/2021/10/02/steppers-and-esp32-make-this-retro-modern-flip-clock-tick/>

在发光二极管变得便宜到无处不在之前，翻转卡显示器几乎是获得数字时钟的唯一方式。这些完全机电设备有其自身的魅力，如今它们有一种复古的标志。不过，除了旧货出售和旧货店之外，它们有点难找到——当然，除非你有自己的东西。

诚然，[[黄大炜]的基于 ESP32 的翻转时钟](https://www.youtube.com/watch?v=8N47ne4M_Lo)与“我得到你了，宝贝”时代的翻转卡有天壤之别。不幸的是，下面的视频是我们了解这个钟背后的故事的唯一线索，但它是不言自明的。[David]通过自己制作翻转卡开始构建，这一过程需要一些拓扑技巧和激光切割机。3D 打印的卷轴上装有卡片，然后将卡片连接到装有步进电机和霍尔效应传感器的框架上。ESP32 通过 L298N H 桥驱动器驱动步进器，但很难说是否有 RTC 芯片或微控制器只是通过 NTP 服务器获得时间。

[大卫]可能不是唯一一个试图重现复古外观的人，但我们不得不称赞他——这是一个很棒的外观，需要一个聪明的制作者不仅能制作这样的时钟，还能制作一个视频，在没有一句旁白的情况下清晰地解释这一切。

 [https://www.youtube.com/embed/8N47ne4M_Lo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8N47ne4M_Lo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[孙斌]给了我们这个提示。谢谢！