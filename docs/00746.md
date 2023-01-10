# Nim 为您编写 C 代码——甚至更多

> 原文：<https://hackaday.com/2018/09/25/nim-writes-c-code-and-more-for-you/>

当我们第一次听到尼姆的时候，我们想到了这个游戏。不过，在这种情况下，nim 是一种编程语言。当然，我们需要另一种编程语言，对吗？但是尼姆有点不同。它不仅是跨平台的，而且不是针对汇编语言或机器码，而是针对其他语言。因此，Nim 程序最终可以由 C 编译，或者由 JavaScript 解释，甚至由 Objective C 编译。最重要的是，它可以生成非常高效的代码，并且开销很低——至少可能是这样。查看[史蒂夫·凯洛克的] [语言快速入门](https://totallywearingpants.com/posts/nim-underdog/)。

事实上，它可以针对不同的编译器后端，这意味着它可以支持您的 PC 或 Mac 或您的 Raspberry Pi。由于 JavaScript 选项，它甚至可以针对您的浏览器。如果你读了史蒂夫的文章，他展示了一个简单的 Hello World 程序是如何以低于 50K 的代价结束的。当然，没有什么是 C 编译器做不到的，这是有意义的，因为 C 编译器实际上是在生成最终的可执行文件，尽管自己去掉所有的开销有点困难。

此外，nim 还提供了许多现代特性和包管理。有垃圾收集，但你可以选择退出，也可以选择如何运行和何时运行。对于大多数东西都有一个非常健壮的库，包括特定于操作系统的代码的包装器和一个外部 GUI 库。

语法很简单，借鉴了 Python 很多东西(包括缩进的敏感性，我们对此有复杂的感觉)。这里有一个来自主[网站](https://nim-lang.org/)的例子:

```

import strformat
type
  Person = object
    name*: string # Field is exported using `*`.
    age: Natural # Natural type ensures the age is positive.
```

```
var people = [
  Person(name: "John", age: 45),
  Person(name: "Kate", age: 30)
]

for person in people:
  # Type-safe string interpolation.
  echo(fmt"{person.name} is {person.age} years old")

```

如果你认为编译成 C 是欺骗，别忘了 C++也是这样开始的。这种语言本身不会对您的可执行文件产生任何依赖，当然，除非您显式地使用一个库。当然，我们更有可能想要建立自己的语言，但是它[可能不会有这么多特性](https://hackaday.com/2018/01/22/tiny-programming-langauge-in-25-lines-of-code/)。顺便说一下，Nim 是我们之前报道过的“[试试看](https://hackaday.com/2017/07/18/the-site-of-a-hundred-languages/)”网站上众多选择中的一个。