# 一个贝壳？一种编程语言？放松点。都是！

> 原文：<https://hackaday.com/2020/08/08/a-shell-a-programming-language-relax-its-both/>

每次我们发布一个使用 shell 脚本的 Linux hack，都会有人插话说编写 shell 脚本有多糟糕。虽然我们喜欢它的无处不在和高效，但我们不能否认 shell 本身就是一个黑客。[Axel Lijencrantz]想把你的 shell 变成一个名为 Crush 的完整的编程语言。

从表面上看，它像一个贝壳。想要查看当前目录的内容吗？简单:`ls`。

区别在下面。在 Crush 中，ls 是内置的，它像数据库一样按行返回数据。您可以使用类似 SQL 的命令来操作数据库:`ls | where {type=="directory"}`。

您仍然可以将 I/O 视为二进制流。但是 Crush 也知道 CSV 文件、JSON、面向行的文件和其他几种格式。因此，如果您试图将`ls`的输出提供给一个程序，并以 JSON 的形式需要它，这很简单:`ls | json:to ./listing.json`。

Crush 还可以进行数学运算，而不需要像以前的 shells 那样使用诡计，也不需要像 bash 那样使用奇怪的语法。shell 支持闭包，您可以将闭包赋给变量，使之成为函数。另一个受欢迎的特性是 Crush 理解名称空间的概念。

有一些奇怪的地方，比如用`%`代替`*`作为通配符，因为`*`是用于乘法的。然而，我们喜欢许多特性，包括简化的远程执行和创建定制类型的能力。

Crush 类似于 [Nu，](https://hackaday.com/2020/05/21/linux-fu-alternative-shells/)，但是在编程语言方面有一些不同的目标。如果您仍然在 bash 这样的传统 shells 中编写程序，请确保运行一个 [linter](https://hackaday.com/2017/03/29/lint-for-shell-scripters/) 。