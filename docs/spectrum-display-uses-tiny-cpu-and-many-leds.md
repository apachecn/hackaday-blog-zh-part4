# 光谱显示使用微型 CPU 和许多发光二极管

> 原文：<https://hackaday.com/2021/06/23/spectrum-display-uses-tiny-cpu-and-many-leds/>

你可能会认为用一个小型的 ATTiny85 制造一个[频谱分析仪](https://www.instructables.com/ATtiny85-Spectrum-Analyzer-on-RGB-Led-Matrix-16x20/)最难的部分是软件。但对[tuenhidy]来说，我们怀疑困难的部分是制造一个由 320 个 led 组成的阵列，这个小处理器可以驱动它。正如你在下面的视频中所看到的，这个设计确实有效。

关键是使用 TPIC6B595N，这是一个 8 位移位寄存器，用于驱动非逻辑输出。所有输出开启时，驱动 fet 可以为每个通道提供 150 mA 电流，器件可以处理每个通道 500 mA 的峰值电流。室温下，该器件的总功耗可能超过 1W，当然，功耗会随着温度的升高而降低。如果你需要更高的功率，有一种 DW 型器件可以多处理几百毫瓦的功率。

一个[定点 FFT 库](https://github.com/kosme/fix_fft)做实际工作。该程序只需读取样本、处理 FFT，并通过移位寄存器驱动 led。

施工技术也有点有趣，因为许多布线都留在 LED 引线上。我们赞赏这一简洁的工作，但我们认为我们在 PCB 走线方面运气会更好。

虽然被宣传为频谱分析仪，但像这样的设备实际上更像是音乐可视化工具。如果你想要一个真正的频谱分析仪，它们已经变得相当便宜。尽管 LED 栅极对于实际输出来说不切实际，但它胜过了[乒乓球](https://hackaday.com/2016/04/28/ping-pong-spectrum-analyzer/)。

 [https://www.youtube.com/embed/257Ma3YemKs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/257Ma3YemKs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



four hundred