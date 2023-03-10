# 用多音量控制器把它混合起来

> 原文：<https://hackaday.com/2020/11/06/mix-it-up-with-a-multi-volume-controller/>

为了黑进别的东西而等着某个东西坏掉有什么用？只要不被利用，谁在乎呢？[OmniSaiRen]有一个百灵达 MIDI 控制器只是占用空间。他们没有出售它，而是决定将其内置到他们肯定会使用的东西中——[一个带有静音键和其他有用宏的多音量控制器](https://relivesight.com/projects/encoder/)。

在掏空外壳后，[OmniSaiRen]给它涂了几层光滑的白色油漆，配上黑色的键帽和旋钮，看起来真的很不错。计划是使用原始的编码器，但是当他们不能让编码器与 Arduino Nano 一起工作时，[OmniSaiRen]用电位计代替了它们。我们很遗憾地报告，Cherry Blues 只成功地建造了这座建筑，因为它们的外壳都是黑色的，而且还到处乱放，占用了空间，但也许[OmniSaiRen]会逐渐喜欢上它们。

如果你厌倦了用鼠标点击来调低音量，你需要做一个这样的东西。它运行在 [deej 上，这是一个开源的音量混合器，可以与 Linux 和 Windows](https://github.com/omriharel/deej) 一起工作，所以你还在等什么？[如果你只想要一个单一的硬件音量旋钮，用旋转式](https://hackaday.com/2020/06/04/rotary-controller-dials-in-pc-volume/)拨它不会错。

通过 [r/duino](https://www.reddit.com/r/arduino/comments/jlklv9/deej_arduino_nano_potentiometers_mx_switches_and/)