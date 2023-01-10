# OpenGL 机器学习运行在低端硬件上

> 原文：<https://hackaday.com/2021/11/13/opengl-machine-learning-runs-on-low-end-hardware/>

如果你研究过 GPU 加速的机器学习项目，你肯定熟悉英伟达的 CUDA 架构。同样，您已经在网上查看了价格，知道获得一个支持这种特定并行编程品牌的高性能显卡会有多贵。

但是，如果你可以在 GPU 上运行机器学习任务，而不使用比 OpenGL 更新奇的东西，那会怎么样呢？这就是[lnstadrum]已经研究了一段时间的东西，因为它将允许像最初的 Raspberry Pi Zero 这样的设备运行图像分类等任务，速度远远快于它们单独使用 CPU 的速度。诀窍是将你的计算任务分解成可以使用 OpenGL 着色器执行的任务，OpenGL 着色器通常用于推动视频游戏图形。

[![](img/be4e71c1aed6c448aebe2474c0a56c00.png)](https://hackaday.com/wp-content/uploads/2021/11/openglml_detail2.png)

An example of X2’s neural net upscaling.

[lnstadrum]解释说，过去十年左右的 OpenGL 版本实际上包括所谓的*计算着色器*，专门用于运行任意代码。但不幸的是，Pi Zero 等主板上没有这个选项，它只符合 2007 年的嵌入式系统 OpenGL(GLES)2.0 标准。

以这样一种方式构建神经网络，使其与这些更受约束的平台兼容，要困难得多，但最终结果有更有趣的应用来展示它。在测试中，Raspberry Pi Zero 和几款较旧的 Android 智能手机都能够以相当高的速度运行预先训练的图像分类模型。

这不仅仅是一些思想实验，[【lnstadrum】发布了一个名为 *Beatmup*](https://github.com/lnstadrum/beatmup) 的图像处理框架，使用这些概念你现在就可以玩。C++库有 Java 和 Python 绑定，根据文档，应该可以在几乎任何东西上运行。框架中包括一个名为`X2`的简单工具，它可以在从笔记本电脑的集成显卡到 Raspberry Pi 的所有东西上执行 AI 图像升级；这使得[成为检验机器学习这一迷人应用的绝佳方式](https://hackaday.com/2021/04/05/ai-upscaling-and-the-future-of-content-delivery/)。

说实话，我们在这一点上有点落后，因为 Beatmup 在今年 4 月首次公开发布。到目前为止，它可能一直在雷达下飞行，但我们认为这个项目有很大的潜力，并希望一旦消息传出，它甚至可以从最低级的硬件中挤出令人印象深刻的结果，就能看到更多。

【感谢伊山的提示。]