# 胸腔灯踢了它一个档次与党的模式

> 原文：<https://hackaday.com/2022/10/01/rib-cage-lamp-kicks-it-up-a-notch-with-party-mode/>

我们认为[Michelle]的[声音反应胸腔灯](https://www.hackster.io/michellesh/sound-reactive-rib-cage-6763a8)非常棒，照片和它是如何制作的细节也同样精彩。这种灯由雕刻和上蜡的木材制成，内部是一束 LED 照明，能够提供各种不同的调色板和图案，包括对声音做出反应的能力。毕竟，每个胸腔都应该有一个派对模式。

[![](img/2fe5d2754b7952c8667852e6bc8d5d44.png)](https://hackaday.com/wp-content/uploads/2022/09/Sound-Reactive-Ribcage-Detail-1.png)

The LED strip is fashioned into an atom-like structure.

事实证明，设计好的胸廓比人们想象的要困难得多。[Michelle]的方法是使用一个解剖的 3D 模型作为参考，追踪每一块，这样它就可以从一块平的木头上切割下来。

然后将制成的平板组装成一叠，每个肋以大约 20 度的角度向下。这个过程本身就是一个巧妙的破解:不是以完全相同的角度钻孔，[Michelle]只是将孔的直径扩大到钢棒直径的两倍。结果呢？这些碎片会自己向下倾斜。

LED 照明本身就是一件不错的作品。基本结构来自焊接实芯线。RGB LED 灯条缠绕在上面，然后用铁丝网加固。结果是一个看起来像原子的结构位于胸腔内。一个 ESP32 开发板通过 [FastLED](https://fastled.io/) 库驱动一切。

一切的代码，包括声音反应的工作位，都依赖于 INMP441 I ² C 麦克风模块[都可以在 GitHub](https://github.com/michellesh/rib-cage) 上获得。如果你想制作自己的声音反应艺术，[一定要看看这些手臂](https://hackaday.com/2021/12/09/sound-reactive-mannequin-arms-make-for-creepy-lounge-decor/)。

想看看活动的胸腔吗？下面嵌入了一个简短的演示视频，演示声音反应。我们认为同样适用于派对或放松模式。

 [https://www.youtube.com/embed/KU6QVG05XLA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KU6QVG05XLA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

