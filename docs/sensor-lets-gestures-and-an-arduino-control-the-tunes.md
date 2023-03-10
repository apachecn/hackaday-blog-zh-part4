# 传感器让手势和 Arduino 控制音乐

> 原文：<https://hackaday.com/2019/08/17/sensor-lets-gestures-and-an-arduino-control-the-tunes/>

每次我们看《少数派报告》时，我们都想在电脑前做出狂野的手势——大多数都是礼貌的。[Rootsaid]想要做同样的事情，并发现 PAJ7620 是一种简单的方式[来读取手势](https://rootsaid.com/arduino-volume-controller/)。这个小传感器有一个串行接口，可以识别相当多的手势。准确地说，该设备可以读取九种不同的运动:上、下、左、右、前、后、顺时针、逆时针和波动。

通用平台上有大量的库可以阅读。如果你有一个 Arduino 可以作为个人电脑的键盘，代码几乎可以自己编写。[Rootsaid]为 PAJ7620 使用一个特定的库，并使用另一个库`Nicohood`来发送媒体密钥。

有了这两个库，编写代码就非常简单了。您只需从传感器读取一个寄存器，并使用`Nicohood`库确定发送哪个密钥。串行通信是 I2C 和有一个微小的光学传感器随着红外发光二极管板载。

当然，您可以发送除媒体控件之外的其他键。例如，我们不介意用一个手势在网页上来回切换。

我们已经看到用[雷达](https://hackaday.com/2017/01/24/millimeter-wave-radar-tracks-gestures/)进行手势识别。我们也用[超声波](https://hackaday.com/2017/11/01/listening-for-hand-gestures/)看到过。

 [https://www.youtube.com/embed/MGeyaiZE4dc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MGeyaiZE4dc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) u