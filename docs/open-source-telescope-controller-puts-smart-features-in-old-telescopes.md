# 开源望远镜控制器在旧望远镜中加入智能功能

> 原文：<https://hackaday.com/2020/04/04/open-source-telescope-controller-puts-smart-features-in-old-telescopes/>

在这种时候，我们都需要超越自我。这个项目可能会有所帮助:OnStep 是一个开源的望远镜控制器，一个控制望远镜指向天空中有趣事物的设备。想看看 M31 吗？使用 PC 或智能手机上的应用程序，选择物体，OnStep 将平移和倾斜您的望远镜，直到仙女座星系出现在视野中。

 [https://www.youtube.com/embed/mOXqw7EN8YE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mOXqw7EN8YE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



智能望远镜并不新鲜:我们已经见过像 [Meade LX90](https://www.meade.com/lx90-telescopes.html) 这样的望远镜，它包括智能控制器，可以使用 GPS 信号计算出时间、位置和指向天王星的方向，并取得不同程度的成功。不过，这些都使用专有控制器，而且一般都很贵。OnStep 设计简单，成本低，可由现成的零件制造。

它完全不依赖于硬件:控制器可以是 Arduino、Teensy 3 甚至是 ESP32。PCB 设计可以与任何这些控制器一起工作。移动望远镜的马达也是如此，所以你可以用你周围的零件来建造这个装置。许多制造步进控制器的人都改装了老式的电动但不智能的望远镜支架。其他人使用旧的支架，用更精确的马达取代缓慢、不精确的马达，使望远镜更加精确和平稳。建立在 OnStep wiki 上的[望远镜画廊](https://onstep.groups.io/g/main/wiki/Showcase%3A-What-Users-Built-With-OnStep)是一个很好的起点，可以看到像这个 [30 岁的 Celestron 望远镜这样的例子，它是通过 OnStep 转换](https://onstep.groups.io/g/main/message/5924)带入 21 世纪的，或者是对[20 世纪 60 年代的望远镜进行的转换，增加了一个智能底座](https://onstep.groups.io/g/main/topic/28863133#6940)。

这是一个看起来很棒的项目，基本的东西都已经整理好了，但是仍然有一群专门的用户在进行工作和改进。虽然在困难时期我们倾向于关注自己，但有时仰望天空，看到星星仍在闪耀，会更好。