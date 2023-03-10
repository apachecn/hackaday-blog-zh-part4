# 深入研究门级键盘接口的细节

> 原文：<https://hackaday.com/2021/04/07/diving-into-the-details-of-keyboard-interfaces-at-the-gate-level/>

永远不要怀疑一个好老师的价值。即使你知道——或者认为你知道——正在呈现的材料，一个好的老师也能开阔你的眼界，用新的方式看待事物，这将会给你带来意想不到的回报。

这是我们在观看[Ben Eater]关于为他的试验板 6502 计算机[构建键盘接口](https://www.youtube.com/watch?v=w1SB9Ry8_Jg)(嵌入在下面)的最新视频时得到的感觉。从表面上看，让键盘与计算机对话应该是一件简单的工作。[本]和[之前研究过老式 PS/2 键盘使用的串行协议](https://hackaday.com/2021/03/11/decoding-the-ps-2-keyboard-protocol-using-good-old-fashioned-hardware/),甚至用分立的移位寄存器芯片构建了一个非常复杂的电路来可视化键盘发送的数据。下面的视频继续这项工作，这一次集中在使用他的 6502 试验板计算机的键盘。

在中断编程的一些有益的预备知识之后，[Ben]开始深入研究从键盘中提取有用信号的逻辑级细节。他的信号处理从一些反相器和一个 RC 网络开始，将多个时钟脉冲转变为一个逻辑电平转换。一步一步地走过这条赛道是真正有趣的部分；即使你知道答案最终将是“施密特触发器”，达到这一点真的很有启发性。

当然，[本]的视频主要完成的是让我们想跟随他，建立一个我们自己的试验板计算机。从低 rez VGA 卡到可靠的 UARTT2，跟随他的分立芯片构建总是有教育意义的。

 [https://www.youtube.com/embed/w1SB9Ry8_Jg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w1SB9Ry8_Jg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

