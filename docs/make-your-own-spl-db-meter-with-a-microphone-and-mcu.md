# 用麦克风和 MCU 制作您自己的 SPL DB 电度表

> 原文：<https://hackaday.com/2019/07/22/make-your-own-spl-db-meter-with-a-microphone-and-mcu/>

SPL(声压级)分贝计之类的测量设备可能看起来令人望而生畏，但[Shawon m . shahriyar][的这篇文章表明，制作自己的](http://embedded-lab.com/blog/making-a-spl-db-meter/)只需要两个基本成分:麦克风和微控制器。显然，麦克风是用来测量声压水平的，然后将其输出馈入微控制器的 ADC，微控制器在将结果发送到显示器之前会进行一些运算。

[Shawon]介绍了必须执行的计算背后的所有理论，然后展示了原型设置所针对的 8 位 MCU 上运行的 C 代码。显示器为图形 LCD 类型，能够显示带有数值的文本以及指示测量水平的条形图。对于测量本身，均方根值取自 16 个 ADC 样本，而算法考虑了[seed-source 麦克风](https://www.seeedstudio.com/Grove-Sound-Sensor.html)模块的规格，特别是其平均 50 dB 灵敏度额定值。

虽然没有提供完整的原理图，但任何人都可以使用几乎任何内置 ADC 的麦克风和 MCU 来构建自己的 SPL dB 电表。文章还指出，选择更高质量的麦克风会产生更好的效果，当然更快的 MCU 会提供更多选项，包括 FFT 处理。由于代码本身相当简单，将其移植到基于 ARM 的 MCU 应该很容易，这样就可以使用 TFT LCD 等器件。

休息之后，来看一下这篇文章中 SPL dB 测量仪的运行视频。

 [https://www.youtube.com/embed/_grNn9yVFz0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_grNn9yVFz0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

