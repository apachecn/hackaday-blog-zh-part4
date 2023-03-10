# 从头开始接收模拟视频无线电信号

> 原文：<https://hackaday.com/2020/05/31/receive-analog-video-radio-signals-from-scratch/>

如果你最近在 RTL-SDR 论坛上，你可能已经看到很多工作已经进入了 DragonOS 软件。这是一个软件定义的无线电小组，他们在专门构建的基于 Debian 的 Linux 发行版上投入了大量的精力，该发行版可以提供大量现成的 SDR。来自他们的最新和最令人兴奋的项目涉及一种使用软件接收和解调模拟视频的方法。

[Aaron]的视频(链接如下)演示了使用一款名为 [SigDigger](https://batchdrake.github.io/SigDigger/) 的特定软件，使用 HackRF 分析来自无人机的模拟视频流。(当然，任何输入的模拟信号都可以使用，不一定是无人机。)该软件显示各种活动频率范围，允许用户缩小到一个频率范围，然后开始解调。虽然它必须以恰到好处的方式来获得任何看起来不像雪的东西，但[Aaron]能够在几分钟内获得可识别的结果。

让这样的东西完全在软件中工作是一个令人印象深刻的壮举，尤其是考虑到这里使用的所有软件都是免费的。当然，这不会像大多数电视台广播的数字信号那样容易，但仍然有很多乐趣。如果你错过了 DragonOS 的发布，[几周前](https://hackaday.com/2020/04/11/software-defined-radio-made-easy/)我们报道了它，从那以后它变得越来越好，这个项目只是一个例子。

 [https://www.youtube.com/embed/PxKs1MXwmp0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PxKs1MXwmp0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

