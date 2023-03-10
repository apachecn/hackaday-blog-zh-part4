# 极简定时器倒计时 LED 矩阵

> 原文：<https://hackaday.com/2021/10/01/minimalist-timer-counts-down-with-led-matrix/>

为了寻找比传统厨房定时器更具风格的东西，[[马丁·乔纳松]决定利用最后几个月的时间，利用旋转编码器、16×9 LED 矩阵和 Teensy 2.0 微控制器来设计和制造他自己的想法](https://github.com/grapefrukt/kitchen-timer)。他本可以把时间花在更好的事情上吗？可能吧。但是你可能不会在这里读到它，所以我们不会为这样的想法而烦恼。

[![](img/696367d58dd9d467edd949b1f1d6c3b3.png)](https://hackaday.com/wp-content/uploads/2021/09/ledtimer_anim.gif) 组装在一块 perfboard 上的手工电路还包括 Adafruit PowerBoost 500 充电器、3.7 V 2500 mAh LiPo 电池、IS31FL3731 Charlieplexed PWM LED 驱动器和压电蜂鸣器。旋转编码器的顶部用一个出售的金属旋钮盖住，结合由堆叠的激光切割 3 毫米丙烯酸板制成的外壳，真正赋予该设备一个非常时尚和优雅的外观。

虽然硬件相当不错，但真正将整个项目整合在一起的是软件。作为一名游戏开发者，[马丁]在计时器的 GPLv3 授权固件上投入了全部。从使用 toneAC 库在倒计时结束时播放旋律，到自定义字体和用户旋转旋钮时暂停计时器的代码，有大量的小触摸应该使计时器成为使用的乐趣。[这些年来，我们已经看到了一些独特的厨房定时器](https://hackaday.com/2016/04/22/nixie-timer-is-easy-to-read-across-the-kitchen/)，但是对细节的关注真的提高了标准。

[Martin]提供了您创建自己的计时器版本所需的一切，包括激光切割案例的 SVG 文件。虽然没有严格要求，但如果你想在这个项目中加入自己的想法，为这个项目定制一个 PCB 将是一个不错的选择。

感谢汤姆的提示。]