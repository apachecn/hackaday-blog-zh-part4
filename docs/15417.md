# 两种深奥的编程语言，一个解释器

> 原文：<https://hackaday.com/2022/11/19/two-esoteric-programming-languages-one-interpreter/>

你们中的许多人可能听说过深奥的编程语言`Brainf**k_`。这是一种几乎不可能使用的示例语言，因为它太简单了。它基本上是一台代码中的图灵计算机——你可以把字符放入一个数组中，读出它们，递增，递减和转移。剩下的就看你的了。祝你好运！

还有比这更糟的吗？Befunge，一种不只是从左到右或从上到下解析代码的语言，而是根据`^, v, >, and <`的使用在任何方向上解析代码。(我们喜欢这个例子中`GOTO 10`看起来像花园小径的样子。)

将两者结合起来，[rsheldii]为我们带来了用 Befunge 编写的`Brainf**k_`解释器 [BrainFunge](https://github.com/rsheldiii/brainfunge) 。令人惊讶的是，由此产生的文章对这两种深奥的编程语言有了足够的了解，使它们有了一点意义。如果你试着跟着读，你肯定会得到 [Esolang Park](https://esolangpark.vercel.app/ide/befunge93) 的帮助，它对我们来说是新的，在显示栈的内容时适应非传统的解析。

如果你尝到了其中的奥妙，你会发现你想要更多，我们已经为你做了一个很好的调查。例如，在 Befunge 上崭露头角之后，我们打赌你会为 [Piet](https://hackaday.com/2020/01/03/a-programming-language-that-lets-you-code-with-pixels/) 做好准备。