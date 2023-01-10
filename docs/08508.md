# 使用 Arduino 从头开始收听调频广播

> 原文：<https://hackaday.com/2020/12/04/fm-radio-from-scratch-using-an-arduino/>

从头开始构建无线电接收机仍然是一个受欢迎的项目，因为它可以在很大程度上使用现成的分立元件和一根足够长的电线来接收无线电信号。无论如何，这对于 AM 收音机来说已经足够好了，但是如果你想听一些与文化更相关的东西，你需要试试这个 DIY FM 接收器。

接收调频无线电波通常比调幅无线电波更困难，因为解调调频信号所需的电路需要进行频率-电压转换，而调幅无线电波则不需要。在这个版本中，[hesam.moshiri]使用了 TEA5767 FM 芯片，因为它能够通过 I2C 进行通信。他还将一个 3W 放大器集成到这个构建中，一切都由 Arduino 控制，包括一个显示当前调谐频率的小 LCD 屏幕。加上一个小的 5V 电源，它也是一个整洁和紧凑的构建。

虽然这个项目中的 FM 接收机不像我们看到的一些 AM 接收机那样从头开始构建，但它仍然是一个有趣的构建，因为它具有小尺寸和 I2C 功能，还因为该构建中的所有元件都有电路原理图。出于这些原因，这可能是进入更复杂的 FM 版本的一个很好的门户项目。

 [https://www.youtube.com/embed/qgci6huZ_-I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qgci6huZ_-I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

