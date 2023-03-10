# 一种自扩展 PWM 驱动器

> 原文：<https://hackaday.com/2019/11/15/a-self-expanding-pwm-driver/>

对于较小的微控制器来说，拥有足够的输出有时是一个挑战。一种常见的解决方案是对可用输出进行某种形式的多路复用，或者使用更高级的方法，如 Charlieplexing，但另一个不错的选择是使用专用驱动板。更好的是，如果你能[菊花链驱动板，以获得更多的输出](http://www.riderx.info/a-self-expanding-esp32-pwm-board/)。

[Eric]一直在做一个 16 通道 LED 项目，但他首先想做一个 8 通道的驱动板。在构建完整的 16 通道版本之前，他意识到他可以采用相同的 8 通道板，制作其镜像，并将其连接到第一个带有接头的板下方，以便将可用通道的数量增加一倍。无需构建单独的 16 通道板，这种快捷方式节省了[Eric]一些时间和大量精力。

这是一个聪明工作而不是努力工作的好例子。8 或 16 通道中的每一个都完全支持 PWM 调光，也可以为电机控制构建类似的电路板。这很好地说明了好的设计最终也能为你所用。如果你需要更多的输出， [Charlieplexing 是获得它们的一种方式](https://hackaday.com/2008/12/03/intro-to-charlieplexing/)。

 [https://www.youtube.com/embed/thRgXC48l54?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/thRgXC48l54?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

