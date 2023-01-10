# 可寻址 7 段显示器可能会使多路复用成为过去

> 原文：<https://hackaday.com/2019/01/12/addressable-7-segment-displays-may-make-multiplexing-a-thing-of-the-past/>

(肖恩·哈金斯)有一种诀窍，可以想出简单的解决方案，可以带来很大的不同，但这是那种“为什么我没有想到这一点？”事情:[可寻址七段 LED 显示屏](https://hackaday.io/project/163228-addressable-7-segment-displays)。

[Sean]的设计基本上是每个人都喜欢的 Neopixel RGB LED 驱动器与无处不在的七段显示器的融合。WS2811 可寻址 RGB 驱动芯片不一定要驱动三种不同颜色的 led，它可以驱动同一显示器的三个部分。由于三个芯片在一个板上，所有七个段加上显示器的小数点可以通过一条数据线来控制。不再有移位寄存器，不再有多路复用。作为一个很好的接触，单个显示器可以通过每个模块背面的连接器组合在一起。[Sean]有一些代码来支持显示，但正在找人来为它建立一个独立的库，所以你可能想参与进来。是的，他计划在他的商店里出售这些主板，但是和他所有的项目一样，这个项目是开源的，你需要的任何东西都可以在 GitHub 上找到。下面的简短视频展示了几个菊花链显示器的运行情况。

像许多[Sean]的设计一样，包括这个 [Arduino 快速设计板](https://hackaday.com/2018/07/28/save-some-steps-with-this-arduino-rapid-design-board/)，这是一个完成繁琐工作的简单方法，它从一个单一的 IO 引脚获得了许多功能。

 [https://www.youtube.com/embed/nfvzyg8gkIE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nfvzyg8gkIE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[0]的提示。