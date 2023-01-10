# 微波采样器就像时域混频器

> 原文：<https://hackaday.com/2022/01/13/microwave-sampler-is-like-time-domain-mixer/>

[Gregory]正在制造一些微波设备，希望将 3.3 GHz 信号转换为 12 MHz 中频。您可能会考虑使用混频器，但您需要一个接近 3.3 GHz 的本振，这不仅难以构建，而且非常接近目标信号，这不是一个好主意。相反，【Gregory】选择了[采样器](https://www.youtube.com/watch?v=yf9qmQQvyh0)，它使用了一种你通常试图避免的效果——[混叠](https://hackaday.com/2017/03/23/say-it-with-me-aliasing/#bandpass-sampling)——以允许用小得多的本地振荡器进行下变频。你可以在下面的视频中看到这个设计。

在将 3.3 GHz 转换为 12 MHz 的情况下，本地振荡器在 100 MHz 左右。这是怎么回事？观看视频，找出答案。最终项目将使 3.3 GHz 信号增加三倍，我们假设 12 MHz 下变频可以使用 PLL(锁相环)轻松锁定频率。

这个电路只不过是一个电子开关和一个电容器。视频的第一部分介绍了操作原理。大约 7 分钟后，白板演示变得更加实用，使用二极管作为开关元件。在最后，我们看到他有一个 PC 板设计，但不是普遍可用。尽管如此，理论上的解释还是值得花 20 分钟观察。

如果你想要一些关于微波齿轮原型的想法，有一些可用的工具。如果你想深入了解[PLL](https://hackaday.com/2016/03/23/unlock-the-phase-locked-loop/)，在之前的帖子中也有很多相关信息。

 [https://www.youtube.com/embed/yf9qmQQvyh0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yf9qmQQvyh0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

