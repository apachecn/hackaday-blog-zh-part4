# 带有扭曲的相机滑块

> 原文：<https://hackaday.com/2020/12/18/a-camera-slider-with-a-twist/>

“范围蔓延”经常被嘲笑为你的想法和完成项目的交付之间的障碍。也许是这样，但有时令人讨厌才是重点。这就是我们如何完成像[这个多轴差动相机滑块](https://www.youtube.com/watch?v=3bU2NGkyh-Y)这样的精彩作品。

我们提到范围蔓延是因为这就是[Jan Derogee]对这个滑块漫长的开发时间及其最终形式的指责。这个设计有点非传统，因为它不仅可以左右移动相机，还可以在平移和倾斜轴上工作，而且它没有在支架上安装任何电机。相反，位于滑轨末端附近的电机通过 217 同步带环将动力传递给托架。有点像 [CoreXY](https://hackaday.com/2019/11/12/core-xy-explained/) 机构；以相同的方向和速度旋转马达会滑动支架，而以相反的方向移动马达会摇动相机。控制器中的 Sparkfun Pro Micro 协调电机以实现平稳的多轴运动，三个步进器——倾斜轴有一个单独的电机——同时工作听起来真的很酷。完整的故事请看下面的视频。

我们之前已经看过[Jan]的一些有趣的项目。看看[他的线性时钟](https://hackaday.com/2018/05/25/linear-clock-is-a-different-way-to-look-at-time/)，磷光显示的[余辉](https://hackaday.com/2018/04/05/persistence-of-phosphorescence-clock-displays-youtube-stats-too/)，或者[他的电脑触摸板](https://hackaday.com/2020/01/22/a-retro-touch-pad-you-can-use-on-modern-computers/)。

 [https://www.youtube.com/embed/3bU2NGkyh-Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3bU2NGkyh-Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

