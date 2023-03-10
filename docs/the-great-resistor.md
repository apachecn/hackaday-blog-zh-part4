# 电阻越大，电阻值越小

> 原文：<https://hackaday.com/2022/11/05/the-great-resistor/>

随着表贴元件迅速成为标准，即使是自制硬件，电阻颜色代码有时也有点过时。然而，任何试图从一堆不同的值中识别随机通孔电阻的人都会知道，这仍然是一项有用的技能。考虑到这一点，[j]决定[用“大电阻”来加大色码的尺寸。](https://hackaday.io/project/188104-the-great-resistor)

![Resistor color code from Wikipedia with white background](img/10a516b36a546f4c8492a7c7c8c1d5fc.png)

How the resistor color-code bands work

该项目的核心是一个 Arduino Nano 克隆和一个分压器，它可以测量测试电阻相对于已知固定值的电阻。使用 16 位 ADC 时，可测量值的范围理论上为 0ω至 15mω，但仍存在一些电气噪声问题，目前将实际范围限制在 100ω至 2mω之间。

[j]正在测量电源电压以帮助抵消噪声，但打算采用过采样/均值方法来改善下一次迭代的结果。

测量值显示在前面的有机发光二极管显示器上，并以电阻器颜色代码显示在后面由 WS2812 RGB LEDs 点亮的巨大符号电阻器上。

![Inside view of the great resistor showing WS2812 LEDs and baffle plates](img/aa4777c15fe2889782810898b943fcec.png)

Inside The Great Resistor, the LEDs and baffle plates make the magic work

除了精度，这个项目看起来非常令人印象深刻，我们喜欢巨型电阻器的构造方式。在科学展览或演示上看起来会很棒。我们确信噪音问题是可以解决的，我们鼓励有这方面经验的读者在下面的评论中提供一些建议。大电阻器被测试后有一个视频！

如果您想了解更多关于电阻色码带的[历史，我们可以满足您的需求。或者，](https://hackaday.com/2020/01/13/why-do-resistors-have-a-color-code/)[用计算机视觉](https://hackaday.com/2015/09/12/resistance-is-theres-an-augmented-reality-app-for-that/)直接读取色码怎么样？

 [https://www.youtube.com/embed/2C_KpQk_63M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2C_KpQk_63M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

