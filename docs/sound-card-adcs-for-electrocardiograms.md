# 心电图声卡 ADC

> 原文：<https://hackaday.com/2019/04/25/sound-card-adcs-for-electrocardiograms/>

大约每隔几年，我们就会被告知，[斯科特]会重新审视制造心电图机的想法。这只是一个有三个电极的小盒子。把它们贴在你的胸部，你会得到一个清晰的心跳读数。这是一个一直做到死的项目，但[Scott]最近的实施非常棒。它很便宜，依赖于每个声卡中几乎荒谬的模数转换能力，并且软件很棒。[正是这种契合度和光洁度让这个项目大放异彩](https://www.swharden.com/wp/2019-03-15-sound-card-ecg-with-ad8232/)。

这种构建的硬件只是一个 [AD8232](https://www.analog.com/en/products/ad8232.html) ，一个设计为任何心电图前端的芯片。然后通过一根 1/8”电缆简单地连接到声卡的麦克风端口。对于特别聪明的人来说，有一个基于运算放大器的版本[。这是一个非常简单的构建，但是和所有简单的构建一样，真正的技巧在软件中。](https://github.com/swharden/diyECG-1opAmp)[这就是这个项目真正闪光的地方](https://github.com/swharden/SoundCardECG)，带有图形的定制软件，足够的信息显示出来，实际上告诉你一些事情。

过去，我们已经看到了许多用于心电图的声卡 ADC，[包括一些以前的产品](https://hackaday.com/2008/05/26/make-an-ecg-with-your-sound-card/)；有道理，声卡是快速获得大量模拟数据的最便宜的方法。你可以看看下面[Scott]的演示视频。

 [https://www.youtube.com/embed/sP_-f5nsOEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sP_-f5nsOEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

