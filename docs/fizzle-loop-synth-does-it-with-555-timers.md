# Fizzle Loop Synth 用 555 个计时器来完成

> 原文：<https://hackaday.com/2019/04/05/fizzle-loop-synth-does-it-with-555-timers/>

对于每一个使用 Arduino 做汤或使用 ESP8266 散列比特币的项目，总会有人重复同样的老调。我本来可以用 555 完成的。这往往是真的，即使它与正在进行的讨论无关。然而，在这种情况下，这样的声明是没有实际意义的。[【孤独冲浪】已经建立了嘶嘶循环合成器，具有不是一个，而是*三个*三镍定时器。](https://www.instructables.com/id/Fizzle-Loop-Synth-V3/)

这是一个既喜欢外观又喜欢性能的建筑。硬件被优雅地嵌入一个老式的金属手电筒外壳中，这个外壳完全被控制所覆盖。这是一种美学，它让我们有一种不可抗拒的冲动去转动旋钮和开关。在内部，两个 555 被设置为基本的闪光灯电路，每个电路为一个 vactrol 供电，本质上是一个阻性光隔离器。内部是一个 LED，它与光敏电阻光学耦合。发光二极管由 555 闪烁，这产生了一个变化的电阻，用于馈给第三个 555 产生音调。

最终的结果是一个有趣的小音箱，能够产生各种各样的哔哔声、哔哔声和哔哔声。如果你需要在外部硬件上记录你的工作，有一个板载扬声器用于在旅途中玩 noodling，还有一个 line-out。如果听到这个电路也连接到一个模块化合成器上，那将会非常有趣。

在古老的 555 上一堂历史课，[我们将为您报道](https://hackaday.com/2018/10/10/the-555-and-how-it-got-that-way/)。休息后的视频。

 [https://www.youtube.com/embed/0eweUEnMdcQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0eweUEnMdcQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

