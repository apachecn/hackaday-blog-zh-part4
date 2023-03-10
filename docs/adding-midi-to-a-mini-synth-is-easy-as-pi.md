# 将 MIDI 添加到迷你合成器就像 Pi 一样简单

> 原文：<https://hackaday.com/2020/09/21/adding-midi-to-a-mini-synth-is-easy-as-pi/>

有一些相对便宜的合成器，如 KORG Monotron，但其中许多都使用不太精确的带状控制器。带状控制器基本上是用手指或手写笔操作的滑动盆。它们被漆成钢琴键的样子，是为了告诉你音符大概应该在哪里。Stylophone 是另一个非常便宜的合成器，它作为合成器的作用甚至更小，并且使用这种类型的输入。如果你不介意不精确，这是一个有趣的输入，但也可能令人讨厌。

[![](img/c2bd1a2372a15662ab40f495b059b36c.png)](https://hackaday.com/wp-content/uploads/2020/09/korg-monotron-pcb.png)【schollz】对这种合成方式不满意，所以[他们使用树莓 Pi 和 DAC](https://schollz.com/raspberrypi/monotron/) 为他们的 KORG Monotron 添加了 MIDI 输入。幸运的是，Monotron 是一个非常容易破解的小合成器，在 PCB 上有漂亮的大标签焊盘。

它真正需要的只是在正确的位置上的几个焊点，加上一个聪明的 Python 脚本。该脚本监听来自键盘的 MIDI 输入，然后控制 MCP4725 DAC，该 DAC 向 Monotron 发送电压。[schollz]写了一个调谐函数，它计算 MIDI 音调的 FFT，以找到每个音调的基频，并将其发送到 Monotron。休息之后来看看。

如果液体控制是你所追求的，但是你只有一个键盘，[试着做你自己的带状控制器](https://hackaday.com/2020/05/03/diy-ribbon-controller-for-a-diy-synth/)。

 [https://www.youtube.com/embed/Winu-9RH_co?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Winu-9RH_co?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/TuBCexYkAv0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TuBCexYkAv0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通路〔t0〕adafruit〔t1〕