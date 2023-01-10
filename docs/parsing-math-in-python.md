# 用 Python 解析数学

> 原文：<https://hackaday.com/2020/09/18/parsing-math-in-python/>

给计算机编程曾经更难。不要误解我们——今天，人们倾向于用计算机解决更难的问题，但编程的基本行为更容易。我们有高级语言、工具包，甚至来自操作系统的帮助。大多数人从来不知道如何直接从磁盘驱动器中读取数据，将数据解块成记录，以及只使用移位和加法来执行乘法。虽然这是一件好事，但有时学习基础知识也是有益的。那是[gne behay]大学学习水平太高时的想法，于是决定用 Python 写一个[算术表达式解析器。它大约有 100 行代码。](https://github.com/gnebehay/parser)

解释数学表达式是那些看起来很简单的事情之一，直到你进入其中。第一个问题是正确地对输入进行词法分析——这个术语的意思是拆分成标记。对于一个人来说，5-3 是三个记号{5，-，和 3}，这似乎很简单，也很容易理解。但是 5+-3 呢？那也是三个令牌:{5，+，-3}。棘手。

优先权是另一个问题。如果看 5+3*2，应该记得答案是 11 或者 5+(3*2)。然而，除了惯例之外，认为答案是 16 或(5+3)*2 也同样有效。另一个惯例是左联想，这样 7-4+2 就是 5 而不是 1。事实证明，[gnebehay 的]解析器目前为该表达式抛出了 1，但他承诺很快会修复它。

虽然阅读代码很有趣，但真正的价值是自述文件，它记录了解析器的创建及其背后的一些理论。这种事情曾经是计算机科学课程的主要内容，但是今天你不太可能遇到它，因为课程关注的是更高层次的结构。

你可能不会用这个代码做任何事情。你很少需要解析一个数学表达式，即使你需要，现在也有很多工具可以帮助你。但是你可能只是学到了一些关于解释器和编译器如何消化文本和获取意义的知识。

今天，您可能会用 [ANTLR](https://hackaday.com/2017/09/07/language-parsing-with-antlr/) 或一些类似的工具构建一个解析器。虽然 100 行看起来很小，但我们已经见过比这更小的[小语种](https://hackaday.com/2018/01/22/tiny-programming-langauge-in-25-lines-of-code/)。