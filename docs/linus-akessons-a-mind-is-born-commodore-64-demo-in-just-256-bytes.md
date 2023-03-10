# 莱纳斯·奥克松的《思想诞生》Commodore 64 演示版仅 256 字节

> 原文：<https://hackaday.com/2021/05/19/linus-akessons-a-mind-is-born-commodore-64-demo-in-just-256-bytes/>

如果说 Commodore 64 演示场景相当惊艳，那也是轻描淡写。对于那些没有意识到的人来说，这里的“演示”本质上是一种技术演示。通常是为了展示特定的效果或其他(视觉)属性，这些效果或属性推动了运行它的平台的极限，或者以一种特殊的方式使用它的硬件。在[Linus kesson]的 [*一个想法诞生了*](https://linusakesson.net/scene/a-mind-is-born/) 演示中，挑战在于尽可能在 256 字节中完成，同时提供视听体验。

虽然乍一看，256 字节听起来似乎很多，但这段代码必须生成通过 Commodore 64 的 SID 音频芯片输出的完整旋律，同时生成有吸引力的视觉模式。这是一项艰巨的任务，比赛结果的视频截图(休息后包括)清楚地表明了这一点。这里的秘方是利用 C64 的 SID 音频和 VIC-II 视频芯片。

在 60 Hz 定时器中断的驱动下，SID 的三个声部分别用于演奏底鼓和低音、旋律和低音，使用线性反馈移位寄存器( [LFSR](https://en.wikipedia.org/wiki/Linear-feedback_shift_register) )创建音乐的总共 64 个小节。这意味着旋律在某种意义上是随机生成的，但确定性足以让人听起来悦耳。

对于视觉方面，C64 在扩展字符模式下运行，使用字体和背景颜色来创建有趣的图案，使用的基本上是一种[细胞自动机](https://en.wikipedia.org/wiki/Cellular_automaton)算法。虽然由于视频数据的覆盖和比赛条件，有一些视觉故障，但这些最终增加了魅力。由此产生的音轨也很吸引人，绝对值得一听。

谢谢你的提示，约翰尼斯！

(那个横幅图像？这就是全部代码。)

 [https://www.youtube.com/embed/sWblpsLZ-O8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sWblpsLZ-O8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

