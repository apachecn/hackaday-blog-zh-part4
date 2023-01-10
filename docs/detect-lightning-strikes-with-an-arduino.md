# 用 Arduino 探测雷击

> 原文：<https://hackaday.com/2021/09/01/detect-lightning-strikes-with-an-arduino/>

闪电是一种强大而看似神秘的自然力量，能够在相对较短的时间内释放出巨大的能量，并且几乎是随机袭击。然而，和其他事物一样，闪电也遵循物理定律，通过一点点技术，它的一些秘密可以被揭开。首先，[只需要一个小的无线电接收器就能探测到雷击](https://hackaday.io/project/181408-sensitive-arduino-lightning-detector-with-ta7642)，【mircemk】向我们展示了如何做到这一点。

当闪电出现时，它也照亮了非常宽的无线电频谱。这个建筑使用一个内置在小型集成电路中的调幅无线电来探测这些无线电波。Arduino Nano 接收来自 TA7642 IC 的信号，并在检测到越来越接近检测器的撞击时点亮一系列 led。当检测到雷击时，白色 LED 闪烁，一些模拟电路支持模拟检流计，该检流计在雷击时也会移动。

虽然这个项目不是我们见过的第一个闪电探测器，但它确实比大多数其他自制产品具有更高的灵敏度。像这样的东西对于游泳池的救生员或经常在外面的工作人员来说是一个有用的工具，但我们也认为它本身就很酷，并且三个网络连接在一起也将使三角攻击成为可能。

 [https://www.youtube.com/embed/2kL7O07zKBU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2kL7O07zKBU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

