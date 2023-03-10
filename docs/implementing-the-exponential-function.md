# 实现指数函数

> 原文：<https://hackaday.com/2020/06/29/implementing-the-exponential-function/>

问普通软件开发人员如何编写指数函数(即 e ^x )的代码，大多数人会告诉你用他们最喜欢的高级语言简单地写一个表达式。但是，相当一部分黑客读者会将微型机器编程到裸机，或者需要比常规实现更高的速度或精度。[Pseduorandom]知道[相当多的计算方法](https://www.pseudorandom.com/implementing-exp)，虽然对于数学恐惧症患者来说这不是轻松的阅读，但这是一次有趣的旅行。

本文涵盖了计算函数的各种方法，包括各种泰勒级数近似、拉格朗日插值和切比雪夫插值。这篇文章有点抽象，但是有 Python 和 C++的例子来帮助它具体化。

这篇论文确实涉及了一些关于为什么你可能想要计算 e ^x 的内容，但是，老实说，我们仍然喜欢[这篇解释得更好的文章](https://betterexplained.com/articles/an-intuitive-guide-to-exponential-functions-e/)，关于它如何与任何持续增长的过程相关联。如果你错过了，你可以看看相关的视频，在下面。我们真希望我们的数学老师向我们解释了这一点。

我们必须承认，如果我们曾经学过这些方法，我们已经忘记了。但是当你不需要在期末考试前死记硬背的时候，你会更容易对数学产生兴趣。

我们承认，如今我们通常对数学更感兴趣。但是我们偶尔会开一个像 [Mathics](https://hackaday.com/2019/05/11/mathics-how-to-do-hard-math-when-youre-not-an-mit-janitor/) 这样的项目。

 [https://www.youtube.com/embed/yTfHn9Aj7UM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yTfHn9Aj7UM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

