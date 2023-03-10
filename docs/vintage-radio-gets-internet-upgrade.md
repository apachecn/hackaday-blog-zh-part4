# 老式收音机获得互联网升级

> 原文：<https://hackaday.com/2021/10/12/vintage-radio-gets-internet-upgrade/>

没有什么比复古硬件更好的了，它的外观和工作方式是值得庆祝的。【老科技。New Spec]对 1964 年的 Dansette 便携式收音机进行了热情的改造，通过赋予它播放互联网电台的能力，同时保留所有原始的控制和外观，将它带入了现代时代。正如他所说，除非你打开它，否则你很难知道它被修改过。

![Internet radio station logos scrolling across small LCD screen](img/690aeb891196f23d775bcd6d0215baa1.png)

A full color LCD behind a convex lens matches the radio’s aesthetic.

这种转换的一个真正的核心是调谐盘的内部已经被全彩色 LCD 显示器所取代，该显示器除了显示其他内容之外，还显示当前正在播放的任何互联网广播电台的标志。LCD 和凸透镜的结合看起来很棒，并且完美地融入了美学。

设备内部是一个 Raspberry Pi，一些简单的 Python 脚本，和一个[盗版音频板](https://learn.pimoroni.com/article/getting-started-with-pirate-audio)。它们一起处理音频流和输出、显示专辑封面以及接受回放控制的输入。一个大的电源库确保了结果的便携性，并且像通常的老式硬件一样，不用担心里面的所有东西。在下面嵌入的视频中观看它的运行。(如果音频板的名字让你兴奋，但你失望地发现没有实际的盗版广播发生？嗯，[树莓派也能做到这一点](https://hackaday.com/2018/04/03/filter-your-pi-and-be-a-responsible-pirate/)。)

 [https://www.youtube.com/embed/98O8wwiskhk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/98O8wwiskhk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

