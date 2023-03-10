# 从 Linux 命令行对您的程序进行拼写检查

> 原文：<https://hackaday.com/2021/05/29/spell-checking-your-programming-from-the-linux-command-line/>

对于我们大多数在高中英语课上表现不好的人来说，拼写检查器是一个真正的游戏改变者。当然，您仍然可以交换“to”和“too”，但是拼写检查器会发现很多拼写错误。但是在你的源代码中呢？你通常不会对源代码进行拼写检查，即使你做了，这些规则也很有趣。毕竟，“my_proejct”是一个非常好的变量名，但是您可能指的是“my_project”这就是一个叫做错别字的程序出现的原因。它的目标是成为一个足够快的源代码拼写检查器，并且有足够低的误报率，这样你就可以对修改过的代码运行它并拒绝拼写问题。

当然，如果“my_proejct”是一次性的输入错误，编译器或解释器可能会发现它。但它不会捕捉评论，也不会捕捉你拼写错误的东西。为此，你需要类似错别字。

您可以包括自定义词典和每种语言的词典。它知道骆驼大小写和蛇大小写，并且知道忽略十六进制代码。我们看到的唯一不好处理的是 C 语言转义。

显然还有其他的检查器，我们从这个项目的比较网格中了解到了它们。有[拼错](https://github.com/client9/misspell)、[拼错](https://github.com/codespell-project/codespell)，还有[拼错](https://github.com/myint/scspell)。这是我们不知道我们需要，但可能需要的工具。

如果您正在编写 bash 脚本，并且想要检查它们的正确性，有 [shellcheck](https://hackaday.com/2017/03/29/lint-for-shell-scripters/) ，它听起来像拼写检查，但是具有完全不同的功能。如果你想提高你的拼写，你可以随时破解一个 [Speak 'n 拼写](https://hackaday.com/2012/12/03/teaching-the-speak-spell-four-and-more-letter-words/)。