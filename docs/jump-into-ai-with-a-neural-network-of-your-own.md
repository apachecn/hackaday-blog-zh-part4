# 用自己的神经网络跳入 AI

> 原文：<https://hackaday.com/2018/10/22/jump-into-ai-with-a-neural-network-of-your-own/>

学习神经网络的困难之一是找到一个足够复杂以至于有指导意义但又不会复杂到阻碍学习的问题。[ThomasNield]有一个想法:创建一个神经网络来学习你是否应该在特定的颜色背景上放置浅色或深色字体。他有一个很棒的视频解释这一切(见下文)和 Kotlin 中的[代码。](https://github.com/thomasnield/kotlin_simple_neural_network)

[Thomas]对优化非常感兴趣，所以他的方法在很大程度上基于数学和优化算法。有一点很方便，那就是已经有了一个算法来做这个决定。他是在 Stack Exchange 上找到的，但我们确信它在某本教科书或论文中。现有的算法使神经网络变得不切实际，但它使训练变得容易，因为你可以通过算法开发一组训练数据。

一旦经过训练，神经网络就能很好地工作。他写了一个小 GUI，你甚至可以在各种模型中进行选择。

不要让科特林让你分心。它是 Java 的衍生物，使用相同的 JVM。代码非常相似，除了它推断类型，还添加了函数式编程工具。然而，所采用的库和原则将适用于 Java，并且在许多情况下，无论您在做什么，这些概念都将适用。

如果你想硬件加速你的神经网络，[有一个棒为那](https://hackaday.com/2018/04/24/neural-networks-on-a-stick/)。如果你更喜欢 C 语言，想要简洁明了的东西，试试 [TINN](https://hackaday.com/2018/04/08/tiny-neural-network-library-in-200-lines-of-code/) 。

 [https://www.youtube.com/embed/tAioWlhKA90?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tAioWlhKA90?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

