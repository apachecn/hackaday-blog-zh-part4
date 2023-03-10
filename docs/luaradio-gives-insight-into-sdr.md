# LuaRadio 让我们深入了解 SDR

> 原文：<https://hackaday.com/2019/12/24/luaradio-gives-insight-into-sdr/>

理论上，开发软件定义无线电(SDR)应用不需要任何帮助。但在现实生活中，你真的不想每次都滚动自己的代码来读取智商样本，对它们执行各种转换，然后驱动音频输出。在最坏的情况下，您将使用一些库(也许是 GNU Radio ),但是通常，您将使用一些更高级的构造，比如 GNU Radio Companion (GRC)。不过，GRC 有点重量级，所以如果你以前觉得它令人生畏，你可能会在 [LuaRadio 网站](https://luaradio.io/new-to-sdr.html)上查看一些材料。

几年前我们已经研究过 LuaRadio，但是从那以后它经历了很多变化，并且有一些优秀的文档。和 Lua 本身一样，LuaRadio 强调快速脚本。它[支持相当多的通用硬件](https://luaradio.io/docs/supported-hardware.html)和几乎任何通过声卡输入数据的东西。

为什么不用 GNU 电台？LuaRadio 有一个[官方答案](https://luaradio.io/docs/comparison-gnuradio.html)。然而，LuaRadio 没有 GUI——至少现在还没有。也许一个黑客阅读器可以解决这个问题。它也不像 GNU Radio 那样成熟，但是它确实有很多积极的特性，比如占用空间小，易于嵌入，以及添加附加特性的简单方式。

如果你有 RTL-SDR，有很多例子:

*   WBFM 广播单声道和立体声接收机
*   NBFM 接收器
*   AX.25 分组无线电接收机
*   POCSAG 接收器
*   RDS 接收器
*   调幅接收机(包络和同步)
*   单边带接收机

project [GitHub](https://github.com/vsergeev/luaradio) 页面显示了最近对版本 0.6.0 的更新。举个例子，这篇文章顶部的流程图在 Lua 代码中是这样的:

```

local radio = require('radio')

radio.CompositeBlock():connect(
radio.RtlSdrSource(88.5e6 - 250e3, 1102500), -- RTL-SDR source, offset-tuned to 88.5MHz-250kHz
radio.TunerBlock(-250e3, 200e3, 5), -- Translate -250 kHz, filter 200 kHz, decimate by 5
radio.FrequencyDiscriminatorBlock(1.25), -- Frequency demodulate with 1.25 modulation index
radio.LowpassFilterBlock(128, 15e3), -- Low-pass filter 15 kHz for L+R audio
radio.FMDeemphasisFilterBlock(75e-6), -- FM de-emphasis filter with 75 uS time constant
radio.DownsamplerBlock(5), -- Downsample by 5
radio.PulseAudioSink(1) -- Play to system audio with PulseAudio
):run()

```

不太难，即使没有太多的文档。如果你更想解决 GRC 问题，我们有一个针对该问题的教程。