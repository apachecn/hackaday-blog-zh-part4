# 附加的多声部合成器也能保存声音

> 原文：<https://hackaday.com/2020/01/13/additive-multi-voice-synth-preserves-sounds-too/>

在[Bruce Land]的微控制器设计课上，他的最后一个项目是[，[Mark]着手制作一个尺寸合适、听起来不错的合成器](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2019/mwa37/mwa37/mwa37/index.html)。我们认为你会同意他确实成功了。不要让那些小按钮欺骗你，因为它听起来不像玩具。

为什么听起来这么好听？原因之一是乐器样本是使用加法合成制作的，这实质上是在每个音符的基频之上叠加泛音。这使得合成器能够更好地模仿自然声音的音色。对于[Mark]弹奏的每个音符，您听到的是由查找表构建的四种频率的混合。这些频率由包络函数整形，从而进一步改善声音。

在声音和功能之间，这是一个相当令人印象深刻的合成器。它可以在钢琴、风琴或拨弦模式下通过一系列八度音阶进行复调演奏。PIC32 运行合成器本身，一对助手 pic 32 可以用来录制歌曲并播放。所以[马克]可以分别录制点和对位法，然后一起回放，或者使用助手图片来微调他的三声部和声。休息过后，我们会为你准备好一切。

如果图片不是你通常选择的，这里有一个 FPGA 合成器。

 [https://www.youtube.com/embed/fTRjps7hm_0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fTRjps7hm_0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

