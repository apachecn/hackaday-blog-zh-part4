# 真正随机的 MIDI 控制

> 原文：<https://hackaday.com/2019/03/09/truly-random-midi-control/>

生成随机数据非常困难，你周围的大多数随机数据并不是真正随机的，而仅仅是伪随机的。对于真正随机的数据，你必须看一些像放射性衰变或者像这样的东西。YouTube 评论者也足够了。使用随机数据生成音符的想法并不新鲜，但是[Danny]的实验性 MIDI 控制器却是另一回事。这是一个移除了控制的 MIDI 控制器，基于放射性衰变生成随机音符。

这个控制器的设计是基于[一个现成的盖革计数器套件](https://www.banggood.com/Assembled-DIY-Geiger-Counter-Kit-Module-Miller-Tube-GM-Tube-Nuclear-Radiation-Detector-p-1136883.html)连接到一个 Arduino。Arduino 代码只是在一个循环中计数，当盖革电子管被触发时，一个中断会触发一点代码来生成 MIDI 音符。这很简单，但是这个项目的优势在于它的文档。[有一本杂志](https://github.com/walkerdanny/cVert/blob/master/documentation/zine.pdf)介绍这个 MIDI 控制器的所有功能。有单音符或音序器功能，一个可定义的根音符和音阶类型，一个八度音程范围，和速度的注意可以设置。

这只是一个 MIDI 控制器，本身不会产生任何噪声，但该设备的视频显示了其范围。[Danny]在一些合成器和采样器的帮助下，从驱动低音线到奇怪的环境音乐。所有的代码和必要的文件都可以在 GitHub 上找到[，下面的视频可以找到](https://github.com/walkerdanny/cVert)。

 [https://www.youtube.com/embed/vMFJ8gjN8Ac?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vMFJ8gjN8Ac?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

