# 弧形突出物制造“不可能”的 3D 打印

> 原文：<https://hackaday.com/2022/12/21/arc-overhangs-make-impossible-3d-prints/>

[3DQue]的一个意外发现使得乍看之下似乎不可能的事情在 FDM 打印机上得以实现。关键是用同心圆弧构建悬垂区域。它也有助于在凉爽的温度下打印，有足够的风扇和较慢的打印速度。除了来自[3DQue]的视频之外，下面还有一个来自[CNC Kitchen]的视频涵盖了这项技术。

如果你想快速浏览，你可能想先从[数控厨房]视频开始。基本思想是，通过制作重叠的小圆弧，使其离零件主体越来越远，从而“在空中”构建曲面。因为弧重叠，所以它们支持下一个弧。结果是惊人的。下面是第三个视频，展示了该工具的一些最新更新。

我们已经看到了用 [fullcontrol.xyz](https://hackaday.com/2022/10/30/playing-with-the-power-of-full-g-code-control/) 手工制作的类似技术，但这是一个 Python 脚本，它半自动地生成必要的重叠圆弧。我们承认表面看起来有点奇怪，但取决于你为什么需要打印突出，这可能只是门票。如果特征在突出物的顶部，也可能有一点翘曲。

除了良好的散热，你不需要任何特殊的硬件。像[CNC 厨房]一样，我们希望这能被主流的切片器所接受。它可能永远不会成为默认设置，但对于可以从该技术中受益的部件来说，这将是一个不错的选择。由于代码在 GitHub 上，也许熟悉主流切片器的人会加入进来，帮助使算法更广泛地可用和自动化。

您将使用这个工具构建什么？如果你不喜欢圆弧，试试看[圆锥切片](https://hackaday.com/2022/11/21/move-aside-planar-im-slicing-my-cone-way/)或非[平面切片](https://hackaday.com/2021/03/08/3d-printing-90-deg-overhangs-with-non-planar-slicing/)吧。

 [https://www.youtube.com/embed/fjGeBYOPmHA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fjGeBYOPmHA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/B0yo-o47688?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B0yo-o47688?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/XSqvxzFnL9g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XSqvxzFnL9g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

