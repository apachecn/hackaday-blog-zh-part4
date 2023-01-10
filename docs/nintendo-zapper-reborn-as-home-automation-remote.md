# 任天堂 Zapper 重生为家庭自动化遥控器

> 原文：<https://hackaday.com/2021/08/07/nintendo-zapper-reborn-as-home-automation-remote/>

一般来说，用枪关灯既危险又昂贵，但对[管道技工]来说，[这就是他做事的方式](https://www.youtube.com/watch?v=-JHT3eCuiMQ)。视频也在休息之后。公平地说，他用的是回收的任天堂 Zapper，而不是火器，并用射频发射器取代了内脏。我们感到震惊的是，他选择了无线电模型而不是红外线，因为他是如何重新利用一把轻型枪的，但我们在*猎鸭*中的分数表明他做出了正确的选择。

发射器来自一个钥匙链遥控器，所以它完全适合 Zapper 机箱。几根电线劫持股票按钮，运行到股票触发器，所以你保持真实的感觉。接收端有点棘手。当它感应到按钮被按下时，它会发送一个脉冲，就像你在车库门开启器中发现的那样，但是为了让灯一直亮着，需要有一些闩锁，所以就有了 Arduino。微控制器记录并操作一个 10 安培的继电器模块，因此它主要充当硬件之间的粘合剂。所有的主要电气部件都装在一个蓝色的塑料盒里，盒子前面有一个插座。

我们不再看到 Zappers 被用于他们的预期目的，因为他们[依赖旧技术](https://hackaday.com/2015/11/16/resurrecting-duckhunt/)，但[并没有阻止人们](https://hackaday.com/2016/02/25/nes-light-gun-turned-video-synthesizer/)重新利用标志性的外围设备。

 [https://www.youtube.com/embed/-JHT3eCuiMQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-JHT3eCuiMQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

