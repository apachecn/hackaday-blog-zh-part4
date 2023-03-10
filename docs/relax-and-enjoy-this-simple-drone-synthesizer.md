# 放松和享受这个简单的无人机合成器

> 原文：<https://hackaday.com/2022/05/29/relax-and-enjoy-this-simple-drone-synthesizer/>

你可能会想，一个能制造如此多噪音和旋钮的合成器应该有十几个晶体管。面板后面的电路肯定很复杂，那里至少有几个 555 定时器，对吗？

但是不，[【lonesoulsurfer】提出的“Beezz 之盒”](https://www.instructables.com/Box-of-Beezz-Drone-Synth/)非常简单。它的灵感来自于一个叫做[“末日循环无人机”](https://www.lookmumnocomputer.com/projects#/circledroneofdoom)的电路，它使用六个可切换的张弛振荡器来发出一些非常酷的声音。Beezz 的盒子在最终版本中增加了一点，在三个可切换的组中有四个振荡器。每个振荡器只有一个晶体管，其浮动基极连接和集电极上的简单 RC 网络。这些张弛振荡器的锯齿波输出可以调整并相加，从而产生一些令人惊讶的复杂声音。看看下面的视频，了解一下 synth 的曲目——我们敢发誓，在某些地方，我们可以听到 [THX 深度音符](https://en.wikipedia.org/wiki/Deep_Note)的元素。

我们探索了一下来理解这些振荡器，看起来这些振荡器符合[雪崩弛豫振荡器](https://hackaday.com/2013/08/06/avalanche-pulse-generator-design/)的条件。[lonesolesurfer]的笔记中指出应该使用 SS9018 晶体管，但在照片中它们似乎都是 2N4401s。我们不确定晶体管在雪崩模式下能工作多久，但是如果它们停止工作，[也许一些氖管会代替它工作](https://hackaday.com/2016/12/12/the-many-uses-of-the-neon-lamp/)。

 [https://www.youtube.com/embed/Lz0C1BahfkU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Lz0C1BahfkU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

