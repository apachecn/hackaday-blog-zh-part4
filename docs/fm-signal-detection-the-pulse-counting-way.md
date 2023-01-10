# 脉冲计数法检测调频信号

> 原文：<https://hackaday.com/2019/08/28/fm-signal-detection-the-pulse-counting-way/>

与解调 AM 无线电信号所需的简单二极管相比，用于 FM 的检波器电路稍微复杂一些。把你的脑袋围在鉴相器、比率检测器、鉴频器和正交检测器周围可能是一个相当大的练习。还有另一种不太常见的解调方法，但谢天谢地，这也很容易理解:[脉冲计数检测器](https://www.youtube.com/watch?v=jQlN2fc7LJc)。

正如[Allan(w2aw)]在下面的视频中指出的，脉冲计数有点用词不当。脉冲计数的工作原理是在接收到的 FM 信号波形的设定点(通常在过零点)产生一个窄的、固定宽度的方波脉冲。由于调制载波的频率发生变化，产生的脉冲序列的占空比也随之变化。这意味着将有固定数量的脉冲，但通过获取脉冲序列的平均电压，我们可以梳理出原始的音频信号。

理论上的简单在实践中往往更为复杂，而[w2ew]详细介绍了这些复杂性，例如需要使用下变频器使脉冲序列中的峰峰值频率偏差更容易检测。这是他的风格，他带领我们通过一个测试电路来证明理论在实践中是可行的。一个简单的双晶体管电路在过零点产生脉冲，一个低通滤波器清理信号，一个廉价的音频放大器再现原始音频。诚然，这是一个粗糙的电路，依靠试验板的杂散电容来工作，但它证明了这一点，并作为进一步实验的起点——也许可以使用 Arduino 来计数脉冲？

我们一直很喜欢[w2ew]的视频，也从中学到了很多。不久前，我们特别推出了他的另一部视频，讲述了射频调制的奥秘。SSB，有人吗？

 [https://www.youtube.com/embed/jQlN2fc7LJc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jQlN2fc7LJc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

