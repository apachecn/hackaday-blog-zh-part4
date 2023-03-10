# Linux-Fu:Shell 脚本和 Here 文档的帮助消息

> 原文：<https://hackaday.com/2020/08/03/linux-fu-help-messages-for-shell-scripts-and-here-documents/>

假设您想在 Bash 或任何 shell 脚本中输出多行文本。也许它是您正在编写的一个特别复杂的 shell 脚本的帮助字符串。您可以为每一行使用单独的`echo`命令。或者你可以在这里使用“[文档](https://linuxhint.com/bash-heredoc-tutorial/)”。

“here document”构造将两个分隔符之间的文本传递给一个命令，就像通过管道传递一样。

```

if [[$# == 0 ]] || [[ "$1" == "-h" ]]; then
cat << EOF
This is my help message. There are many like it but this one is mine.
My help message is my best friend.
EOF

```

所有的文本，包括换行符、空格等等，都被传递给`cat`，你的有用的格式化信息被打印给用户。

您可以在命令提示符下交互使用这些文档，并且可以在函数中使用它们:

```

#!/bin/bash
help() {
    cat << EOF
Here is your help.
EOF
}
```

## 关于此处文档的更多信息

不仅仅是编写帮助脚本，这里的文档在任何时候你想输入多行并把它们连接到一个命令时都是有用的。我们最常直接在 shell 中使用它们。然而，还是有一些细微的差别。

您可能已经知道上面例子中的“EOF”字符串标记了 here 文档的开始和结束。没什么特别的。您可以使用文档中没有出现的任何单词。因此“< < END_OF_HERE_DOC”将起作用。

文档字符串的结尾必须在一行的开头，并且是单独的。前后都不应该有空格。使用一些奇怪的字符作为结束字符串通常是一个好主意，尽管——从理论上讲——你甚至可以使用单个字符。

但是这个需求打乱了代码缩进——参见上面的`help()`函数。如果在重定向括号和字符串之间加一个破折号，shell 将消耗所有前导制表符(但不是空格！).这可以让你缩进你的信息，这样它就不会一起运行。但是在这里，你必须小心声明中的空格:`cat <<- EOF`和`cat <<-EOF`有效，而`cat << -EOF`无效。(它需要分隔符“-EOF”。)不过，如果你能做好，它允许你缩进你的代码，并使用制表符而不是空格。

```

#!/bin/bash 
help() { 
    cat <<- EOF 
        Here is your help. 
    EOF 
} 
```

## 代替

有一点可能不明显，那就是 here 文档可以处理变量扩展。尝试键入:

```

cat << EOF
Your path is $PATH
Your prompt is $PS1
EOF

Your path is /usr/local/sbin:/usr/local/bin:...
Your prompt is ($HOSTNAME \w)\$

```

这甚至适用于命令替换之类的事情。例如，你可以把东西放进`$(ls)`。不过，有时候你不想这样。在这种情况下，只需引用结束字符串。例如:

```

cat << "EOF"
Your path is $PATH
Your prompt is $PS1
EOF

Your path is $PATH
Your prompt is $PS1

```

## 怪癖

你甚至可以把输入发送给一个程序，它什么也不做，就像看起来很奇怪的`:`。但是有些人用它来注释掉大块的脚本，用于调试或其他目的。这有点浪费，因为您不想要的行被放在一个临时文件中，并被输入到一个会忽略它们的程序中，但您可能会看到它完成了。

显然，文档在这里是小众的。我经常使用它们在脚本中编写帮助字符串，但它们只是当你需要在脚本中传递多行或者当你在`stdin`中键入多行时传递给脚本的入场券。