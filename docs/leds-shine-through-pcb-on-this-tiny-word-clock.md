# 发光二极管通过印刷电路板照射在这个微型字钟上

> 原文：<https://hackaday.com/2019/03/27/leds-shine-through-pcb-on-this-tiny-word-clock/>

似乎每个人都喜欢单词钟。也许这是一个空白表面点亮的神秘，以模糊的格式拼凑时间，或者也许它回想起那些虚度了许多小时的“找单词”谜题。不管它是什么，我们看到了很多字钟的构建，但有一些东西特别是关于这个小小的 PCB 字钟的，我们觉得无法抗拒。

像所有有趣的项目一样，[sjm4306]发现自己经历了这个项目的设计过程。基本想法——使用 PCB 作为字符阵列的掩模——非常聪明。我们总是发现激光切割的遮罩有所欠缺，特别是在那些带有所谓的[计数器](https://en.wikipedia.org/wiki/Counter_(typography))的字符中，那些封闭的空格，比如大写 A 或 Q 中的空格，会被激光切割机移除。设计的字符掩模 PCB [sjm4306]使用铜和黑色阻焊膜来形成字母，当其背后的 SMD LEDs 阵列照亮时，会在深色背景下发出令人愉悦的蓝绿色。尽管他尽了最大努力，但相邻电池的光还是透过来了，所以他打印了一个支架，为每个 led 安装了挡板。这个时钟看起来很棒，甚至有一些增值模式，比如一个下降的字符显示一个 la *矩阵*，一个类似 *Pong* 的模式，以及一个看起来有点像*俄罗斯方块*的东西。更多细节请看下面的视频。

我们以前见过单词时钟与计数器问题发生冲突，有些通过[求助于模板字体](https://hackaday.com/2019/03/09/rgb-word-clock-doesnt-skimp-on-the-features/)解决了这个问题，其他的[没有](https://hackaday.com/2018/12/26/word-clock-dont-need-no-stencil-font/)。不过，这个解决方案给我们留下了深刻的印象，以至于我们希望[sjm4306]能够提供 PCB 文件，以便我们能够构建一个。

 [https://www.youtube.com/embed/fYtS_n_GhCY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fYtS_n_GhCY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

