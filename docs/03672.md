# 本周失败:不会说话的 Arduino 对讲机

> 原文：<https://hackaday.com/2019/07/28/fail-of-the-week-the-arduino-walkie-that-wont-talkie/>

Arduino 对讲机出了严重的问题。]建成。

这个想法很简单:建立一个无线对讲机，这样一群摩托车骑手就可以实时通话。是的，这样的产品在商业上是存在的，但是那一点也不好玩。只要有一点聪明才智和一个库存充足的零件箱，这样的设备应该很容易以低廉的价格制造出来，对吗？

显然不是。【GreatScott！]采用了基于 Arduino 的设计，部分原因是因为熟悉微控制器，但也因为便宜且容易获得的 nRF24 2.4 GHz 音频流模块使项目的 RF 部分看起来更容易。试验板上的一切似乎都很简单——一个运算放大器来增强电容麦克风的信号，这是一个有点低但可能对 ADC 有用的 16 kHz 采样速率。无线电模块连接起来了，但是音频质量严重失真。

【GreatScott！]认为试验板上的鼠窝跳线是罪魁祸首，所以他直接跳到了 PCB 构建上。这是一个合乎逻辑的步骤，但似乎这可能是他出错的地方，因为 PCB 版本甚至更糟。我们可能会首先隔离试验电路板电路的问题；失真是来自音频阶段吗？或者也许数字化带来了一些扭曲？或者失真可能来自 RF 级？在进入最终设计之前，我们想回答几个类似的问题。

我们喜欢[GreatScott！]对公布他的失败毫无异议——我们已经报道了[他的次优 CPU 手工器](https://hackaday.com/2016/11/12/how-not-to-build-a-cpu-hand-warmer/)和[他的 3D 打印 BLDC 电机定子](https://hackaday.com/2018/12/18/can-you-3d-print-a-stator-for-a-brushless-dc-motor/)也是一个失败。对这些事情进行事后分析以避免类似的命运总是好的。

 [https://www.youtube.com/embed/SZYwvvh6m-s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SZYwvvh6m-s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

