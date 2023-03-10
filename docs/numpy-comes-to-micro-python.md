# Numpy 来到微 Python

> 原文：<https://hackaday.com/2019/10/29/numpy-comes-to-micro-python/>

[Zoltán]提交了他为 micropython 开发的非常有趣的类似 NumPy 的库 ulab。

他在 MicroPython 中有一个项目，需要在微控制器上进行非常快速的 FFT，当他考虑所有选项时，突然想到一种更结构化的方法，就像我们都知道并喜欢的 CPython 中的方法，也可以在微控制器上实现。因此，他最终得到了一个 python 库，它执行 FFT 的速度比纯 Python 实现快 50 倍，同时提供了 NumPy 和 Python 共同提供的可读性和易用性。

这很酷，更酷的是[Zoltan]写了关于使用库的优秀文档。该文档不仅可以用于他的库，还提供了许多关于如何使用 MicroPython 本身的优秀示例。

我们真的建议 Python 和 NumPy 的粉丝们看一下这个！