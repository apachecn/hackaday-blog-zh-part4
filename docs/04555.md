# 专有风扇吹，获得 PWM 升级

> 原文：<https://hackaday.com/2019/10/26/proprietary-fan-blows-gets-pwm-upgrade/>

专有组件是任何敢于尝试和修理自己硬件的人的克星。不标准的尺寸，缺乏标签或文件，以及没有备件都是意料之中的事。[Jason]很不幸，他有一台旧的戴尔电脑，上面有一个坏的专有冷却风扇，他不得不[做一些有趣的修改来替换它](https://ripitapart.com/2019/10/15/quick-hack-converting-a-computer-fan-from-thermostatic-to-pwm-control/)。

最初的风扇有三根电线，是恒温控制的，这意味着一个小的[热敏电阻](https://en.wikipedia.org/wiki/Thermistor)会随着温度的升高而加快风扇的速度。当然，如今控制 CPU 风扇的标准方式是使用 PWM，因此他构建了一个电路，该电路本质上是将来自主板的 PWM 信号转换为幻像热敏电阻。更令人印象深刻的是，它只需一个 MOSFET 和一个齐纳二极管就能实现。

不幸的是，有一个陷阱。该电路仅单向工作，这意味着风扇速度不会报告给主板，操作系统认为风扇出现故障。但是[Jason]只是禁用了警告，不再过问这个问题。如果你根本不想用 CPU 风扇，你可以把你的整个电脑浸在矿物油里。