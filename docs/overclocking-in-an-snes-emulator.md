# SNES 仿真器中的超频

> 原文：<https://hackaday.com/2019/08/14/overclocking-in-an-snes-emulator/>

bsnes 模拟器有[一个新的超频模式](https://www.reddit.com/r/emulation/comments/cndw4v/bsnes_v1081_overclocking_demonstrations_nightlies/ew9da0h/)来消除 snes 游戏中的减速，同时保持游戏速度准确。我们在功能强大得多的现代机器上模仿旧的 SNES 硬件。消除减速应该是微不足道的吧？对于像 bsnes 这样的仿真器来说，这个问题绝对不简单，因为 bsnes 是为了在仿真时达到像素级的精度而编写的。留下来了解原因。

超级任天堂是一个令人印象深刻的系统，在当时——大部分时间。SNES 帧速率被锁定在 60 FPS，考虑到 NTSC 标准只有 30 FPS，这有点令人惊讶。NTSC 要求每秒 30 帧，但那些是隔行扫描帧。偶数扫描线每秒更新 30 次，奇数扫描线每秒更新 30 次。因此每秒 60 次，屏幕的一半被更新，在偶数和奇数行之间交替。

在每一帧的顶部，半条扫描线的当量标志着该帧的其余部分是偶数还是奇数扫描线。为了产生清晰的 60 FPS，SNES 没有隔行扫描，只是总是写入相同的 240 条扫描线。这也是为什么复古游戏机在现代显示器上看起来如此可怕。空白扫描线被 CRT 电视的模拟模糊性所掩盖。

SNES 主处理器运行所有的游戏逻辑，每秒钟更新图形 60 次，在电视开始将每一帧写入屏幕之前完成每一帧的计算。游戏通常被精心编写，以确保每一帧的处理能在 16 毫秒的窗口内完成。

大多数游戏都有几个场景，其中很多事情同时发生，处理器跟不上帧率。在这种情况下，游戏开始滞后。由于帧速率很难同步到 60fps，所以只需再次显示前一帧，在处理完成时，游戏会暂停该帧。

 [https://www.youtube.com/embed/Q8ph2OVqZeM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Q8ph2OVqZeM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



bsnes 解决方案很聪明。添加了虚拟扫描线，但暂停了音频和视频仿真。这使得整个过程可以非常快速地进行，同时继续与正常的 60 FPS 同步。下面是 Gradius III 演示，展示了结果。

 [https://www.youtube.com/embed/viw3xMTXX40?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/viw3xMTXX40?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



头图:Sandos ( [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:SNES_800.jpg) )。