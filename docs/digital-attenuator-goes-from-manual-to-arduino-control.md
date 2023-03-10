# 数字衰减器从手动变为 Arduino 控制

> 原文：<https://hackaday.com/2018/07/21/digital-attenuator-goes-from-manual-to-arduino-control/>

[Kerry Wong]遇到最酷的硬件，并且总是设法用它做一些有趣的事情。他的小工具 du jour 是一个数字 RF 衰减器芯片的旧演示板，它可以根据一些 DIP 开关的设置以离散的步骤填充信号。[Kerry]的目标:[忘记手指开关翻转，将衰减器置于 Arduino 控制之下](http://www.kerrywong.com/2018/07/15/controlling-an-hmc624lp4e-rf-attenuator-using-arduino/)。

像往常一样，在他的视频中，[Kerry]给了我们一个关于他正在使用的硬件背后的理论的概要。问题中的芯片是一个有趣的怪兽，来自 Hittite 的 HMC624LP4E，该公司于 2014 年并入 ADI 公司。现在已经过时的设备是一个单片微波集成电路(MMIC)，建立在砷化镓衬底上，而不是硅上，并在 64 步内将 DC 衰减到 6 GHz 信号，降至-31.5 dBm。在使用 DIP 开关对电路板进行功能检查后，他很快创建了一个 Arduino 项目，用内置的串行接口控制芯片。目前这只是一个原型，但旋转编码器比扳动开关要方便得多，一旦它被装箱，它将成为[Kerry]射频工作台的一个很好的补充。

如果这个视频让你处于一种射频状态，看看[Kerry]的其他一些视频，比如[这个关于温度补偿晶体振荡器的视频](https://hackaday.com/2018/06/05/drifting-instrument-presents-opportunity-to-learn-about-crystal-oscillators/)，或者[微波电子的奥秘](https://hackaday.com/2017/09/11/doppler-module-teardown-reveals-the-weird-world-of-microwave-electronics/)。

 [https://www.youtube.com/embed/6-pVbwjH5es?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6-pVbwjH5es?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

