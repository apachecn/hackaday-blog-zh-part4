# 用存储器有限的 MCU 驱动电子纸显示器

> 原文：<https://hackaday.com/2022/11/21/driving-e-paper-displays-with-memory-limited-mcus/>

人们很容易对现代微控制器感到厌倦:只需几块钱，你就可以得到一个功能强大的微控制器，足以与 90 年代初的台式计算机相媲美，同时还集成了 WiFi 和蓝牙等当代技术。对于许多项目，我们甚至不必考虑优化我们的代码，因为我们甚至没有触及硬件能力的表面。

但有时你没有使用最新和最大的芯片的奢侈，必须发挥你的手牌。这是像拉里·班克这样的人真正闪光的时候。在最近的一篇文章中，他回顾了他用 8 位 MCU 驱动电子纸显示器(特别是回收的电子货架标签)的实验，这些 MCU 在纸面上不应该有运行它们的资源。

[![](img/df520c03d9f5b4f50fb71eef0e889fb6.png)](https://hackaday.com/wp-content/uploads/2022/11/epapermcu_detail.jpg)

A similar trick can be used on OLEDs

问题是，这些显示器通常希望获得完整的图像，这很容易超过低端芯片上的空闲 RAM。例如，一个 1 位 128 x 128 的图像将消耗 2 KB 的 RAM，是 ATtiny85 上可用内存的四倍多。

正如[Larry]所解释的，他的替代方法是将数据以只有一个字节宽的列写入显示器。结合他在受限硬件上使用[图像解压缩的现有工作，他能够使用 Arduino UNO 快速绘制全屏 TIFF 图像，如休息后的视频所示。他希望这项工作能激励其他人尝试使用二手货架标签上常见的](https://hackaday.com/2021/07/17/png-image-decoding-library-does-it-with-minimal-ram/)[微型微控制器的可能性。](https://hackaday.com/2019/02/25/e-ink-price-tags-fall-off-store-shelves-onto-your-workbench/)

 [https://www.youtube.com/embed/Ow_Yd7A_qEU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ow_Yd7A_qEU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

