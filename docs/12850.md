# 现代 TI 图形计算器上的光线跟踪

> 原文：<https://hackaday.com/2022/02/21/ray-tracing-on-a-modern-ti-graphing-calculator/>

一些不切实际的事情并不是不去做的任何理由，这就是为什么现在几乎任何有 CPU 的东西都可能运行毁灭。出于同样的原因，显然有一种方法可以在现代 TI-84 Plus CE 图形计算器上进行 3D 场景的光线跟踪。这对于任何一个有计算器的人来说都是一个好消息，同时也有很多时间，也许是在无聊的课堂上。

正如[TheScienceElf]在一个[视频中展示的那样，](https://www.youtube.com/watch?v=rY413t5fArw)也是在休息后嵌入的，这并不是人们所期望的英伟达 RTX 30 系列 GPU 的实时体验。尽管在[的计算器](https://en.wikipedia.org/wiki/TI-84_Plus_series#TI-84_Plus_CE_and_TI-84_Plus_CE-T)中基于 [eZ80](https://en.wikipedia.org/wiki/Zilog_eZ80) 的 CPU 比许多 20 世纪 80 年代家用电脑中的 Z80 要高效得多，但标准分辨率下的演示场景需要大约 12 分钟来渲染，正如 [GitHub 项目](https://github.com/TheScienceElf/TI-84-CE-Raytracing)页面上所指出的。

也许这个项目最有趣的部分是它为 TI-84 Plus CE 使用了基于 Clang 的 C & C++ [工具链，这使得访问计算器的硬件和相关内容变得容易，包括图形、文件 I/O、字体、键盘输入等等。即使使用 TI-84 加 CE 来渲染下一部 Pixar 级别的电影不是这些设备可以想象的最有成效的使用，但这个项目和 CE 工具链使修补这些 150 美元的设备变得太容易了。](https://ce-programming.github.io/toolchain/)

它也将提供一个很好的节奏变化，而不是用藏语写 Snake，这是一种基本的方言，顺便提一下,[TheScienceElf]也用藏语写了一个光线追踪器。

(感谢[poiuyt]的提示)

 [https://www.youtube.com/embed/rY413t5fArw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rY413t5fArw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

