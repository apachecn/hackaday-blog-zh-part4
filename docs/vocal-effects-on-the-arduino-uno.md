# Arduino Uno 的声音效果

> 原文：<https://hackaday.com/2020/03/12/vocal-effects-on-the-arduino-uno/>

一想到音频处理，人们通常不会想到 8 位微处理器。尽管如此，如果你正在寻找一些花哨的乐趣，这是完全可能的，[正如[Amanda Ghassaei]在这个 2012 年的复古项目中用 Arduino Uno 展示的那样。](https://www.instructables.com/id/Arduino-Vocal-Effects-Box/)

该构件是基于颗粒合成的思想为声音效果而设计的。在这里，音频样本被分割成小块，称为“颗粒”，并以各种方式进行处理，以发出有趣的声音。盒子上的控制允许用户修改所产生的声音的性质。

[Amanda]的项目是在 Arduino Uno 上运行音频处理的一个很好的例子。有指南介绍如何将片上 ADC 用作麦克风输入，以及如何构建电阻梯形 DAC 输出。作为必要条件，这还需要讨论如何直接写入 ATMEGA 的 IO 端口，而不是使用 Arduino 项目中通常使用的较慢的 digitalWrite()函数。对于任何在微控制器平台上学习音频的人来说，这里都有很多价值。

总的来说，这是一个有趣的项目，对于那些热衷于数字声音处理的人来说是一个很好的入门。当然，那些想要加快速度的人也可以去看看 Teensy 音频库。休息后的视频。

 [https://www.youtube.com/embed/bZ-r_aKuyrE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bZ-r_aKuyrE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

