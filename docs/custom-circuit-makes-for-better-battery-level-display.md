# 定制电路有助于更好地显示电池电量

> 原文：<https://hackaday.com/2018/07/13/custom-circuit-makes-for-better-battery-level-display/>

不都是这样吗？教科书上有一个电路，甚至是一个芯片，设计来做你想做的事情——几乎是完全正确的。对于您的应用程序来说，它有 80%是完美的，而不是接受那 20%，您决定从头开始设计自己的解决方案。

就是那个位置【伟大的斯科特！]发现自己在用[这个定制的 LED 电池电量指示器](https://www.youtube.com/watch?v=rZq2v7two1s)。随着下面视频的展开，我们了解到他并没有完全从零开始。他的第一关是完全明智地使用了 LM3914 10-LED 条形图驱动芯片，这款设备已经运行 VU 电表等产品 40 多年了。该芯片内置梯形比较器和 1 千欧电阻，根据相对于外部电阻设置的上限和下限的输入电压，点亮 10 个 led。不幸的是，固定的内部电阻使其成为线性标度，与他所监控的电池组的放电曲线不匹配。因此，从 LM3914 数据手册中提取设计元素，[太棒了！]利用 LM324 四路运算放大器开发了自己的六 led 显示屏。trimmers 让他调整曲线以匹配电池，而不是每个阶段都有固定的电阻，现在他更有信心知道剩余的电池寿命。

也许是 18650 电池组【伟大的斯科特！]正在建造的是为了他最近一直在做的电动自行车。如果是的话，我们很高兴看到他点焊了端子，不像[最近的电动自行车电池组制造](http://hackaday.com/2018/07/03/an-e-bike-battery-pack-without-spot-welding/)可能会有一些问题。

 [https://www.youtube.com/embed/rZq2v7two1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rZq2v7two1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

