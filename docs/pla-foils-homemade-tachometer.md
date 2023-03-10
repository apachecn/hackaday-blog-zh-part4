# 解放军箔国产转速表

> 原文：<https://hackaday.com/2018/11/22/pla-foils-homemade-tachometer/>

[Integza]建造了一个特斯拉涡轮机，并想知道它的旋转速度。但是，他没有转速表，也不想买。在尝试分析音频以测量速度的错误开始后，他决定使用一种可靠的方法。让车轮打破一个红外线(IR)光遮断器，并在车轮经过时数一数轮辐。如果你知道辐条之间的间距，你就可以计算速度。只有一个问题:[没用](https://www.youtube.com/watch?v=Y9OwuECp6AA)。

事实证明，PLA 对 IR 至少有些透明。知道在轮子上固定一些胶带来阻挡红外线是一件简单的事情，这样事情就会好得多。如果你错过了他建造涡轮机的视频，你可能想先看一下。

结果很好。多亏了互联网，[Integza]能够从一个九岁的乌克兰人那里获得一些代码，并以此为基础。凭借呼吸力，他获得了相当好的旋转，但使用空气压缩机，他轻松打破了 10，000 转/分钟。

我们很惊讶音频方法没有成功。我们知道大公司和其他公司一起花钱听压缩机运转，并决定它们是否会出故障。我们怀疑通过 GNU Radio 或其他 DSP 软件的一些音频处理可以恢复实际的信号，但我们不知道。

如果你以前没有见过特斯拉涡轮机，它使用[无叶片](https://hackaday.com/2016/06/17/micro-tesla-turbine-is-an-engineering-tour-de-force/)并且非常高效。他们可能没有刀片，但他们可以有[硬盘驱动器盘片](https://hackaday.com/2011/09/09/engine-hacks-tesla-turbines/)。

 [https://www.youtube.com/embed/Y9OwuECp6AA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y9OwuECp6AA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

