# 单个的新像素构成了这把光剑的剑刃

> 原文：<https://hackaday.com/2019/08/09/individual-neopixels-make-up-this-lightsabers-blade/>

光剑是《星球大战》系列中的标志性武器，设计成各种形状和颜色。也有一些粉丝制作的版本，其中相当一部分使用了几乎无处不在的 neopixel。[提瑞诺思]决定使用一系列新像素制造他的第一把光剑[，但决定采用一种独特的制造方法。](https://imgur.com/a/XC3lPFN)

[Tirenoth]选择在 5 毫米 LED 外形中使用一堆新像素，而不是通常的条状新像素。[Tirenoth]将每个 LED 的 5v 引脚和 GND 引脚焊接到下一个相同的引脚上，将每个 LED 旋转 180 度，建立一个像素塔。数据输入和输出引脚也焊接到下一个(和上一个)LED 上。这使得 led 系列在物理上更加稳定，并允许它们紧密堆叠在一起，一个在另一个之上。

为了控制新像素，使用了一个[ProFi board](https://fredrik.hubbe.net/lightsaber/v4/)，一个开源的光剑控制器。Proffieboard 使用 STM32 微控制器，允许您连接 led 或 neopixels 以及扬声器。它的开源软件允许像素动画和声音播放。它是专门为光剑版本设计的，通过 Arduino IDE 编程。

[Tirenoth]有一些很好的构建过程的图片，当然也有一些最终结果的图片。不过，他认为这把剑会在战斗中首先断裂。这些年来已经有了一些光剑版本，比如这把[光剑和狂欢模式](https://hackaday.com/2017/09/16/a-lightsaber-with-rave-mode/)，或者这把[光剑用真正的激光制作](https://hackaday.com/2019/01/04/a-foggy-lightsaber-build/)。

via [Reddit](https://www.reddit.com/r/DIY/comments/cmjr34/my_lightsaber_build_with_proffieboard_and) 。