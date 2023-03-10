# 有趣的频谱图绘制和编码

> 原文：<https://hackaday.com/2021/02/26/spectrogram-drawing-for-fun-and-coding/>

在第一个光谱瀑布显示被创造出来之后，在有人尝试创造一个可以在瀑布中产生图像的波形之前，这可能不会花很长时间。我们不知道这位先驱是谁，但自从 Aphex Twin 在他们的音乐中使用这一技术以来，已经有 20 多年了，所以这不是什么新鲜事。如果你想亲自尝试一下， [[Gokberk Yaltirakli]有一个项目适合你](https://www.gkbrk.com/2021/02/spectrum-drawing)，使用一点 Python 代码，用图像文件的 SDR 创建瀑布图像。

这里的价值不一定在于创造比特币标识的瀑布(可以在他放在页面上的视频中看到)，而是在于为特别提款权创造 I 和 Q 值的简单解释。代码有点慢，所以把它的值写到一个由 HackRF 输出的文件中，但是如果你也想要一个 Aphex Twin moment，它可以很容易地被任何其他有能力的输出设备使用，比如 GNU Radio 和声卡。[显示频谱瀑布的硬件甚至不必非常复杂](https://hackaday.com/2011/07/11/waterfall-signal-visualizer-from-arduino-and-cellphone-lcd/)。

谢谢[利奥]的提示。