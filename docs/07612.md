# 视频压缩解释器——就像我们是五岁的孩子

> 原文：<https://hackaday.com/2020/08/28/video-compression-explainer-like-were-five-year-olds/>

[Ottverse]正在开发一个有趣的系列来揭开视频压缩的神秘面纱。最新的部分承诺[解释离散余弦变换](https://ottverse.com/discrete-cosine-transform-dct-video-compression/)就像你是五岁小孩一样。

我们会坦诚相待。五岁时，我们可能不知道如何解释这句话:

> …离散余弦变换采用一组 N 个相关(相似)的数据点，并返回 N 个去相关(不相似)的数据点(系数),其方式是仅在几个系数 M 中压缩能量，其中 M << N

尽管如此，解释还是很清楚的，我们真的很喜欢用球体和星座中的星星来类比。

一个五岁的孩子可能也不知道 Matlab 代码的例子，但是我们喜欢它。我们认为，任何人都可以理解删除太多数据(高压缩)导致图像质量差的实际结果，但即使 75%的数据消失，图像质量也相当好。

所以，虽然你可能不想给你五岁的孩子看这个，但你可能会喜欢它，甚至会学到一些东西。这个系列的其他部分也很不错。有关于数据压缩、编解码器和编码器的讨论。我们相信还会有更多。

如果你不喜欢 Matlab，你可能很容易用 [SciPy](https://hackaday.com/2017/06/26/simple-wave-generation-in-python-and-scipy/) 做同样的事情。或者，试试类似于 Matlab 的几个开源项目之一的 [Octave](https://hackaday.com/2016/06/30/tutorial-on-signal-processing-in-linux-with-octave/) 。