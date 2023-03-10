# Linux Fu:混合 Bash 和 Python

> 原文：<https://hackaday.com/2021/05/04/linux-fu-mixing-bash-and-python/>

尽管 bash 脚本经常遭到诽谤，但它们确实具有某种简单性和易于创建的特点，这使它们难以抗拒。但是有时候你真的需要用另一种语言做一些繁重的工作。我将讨论 Python，但是实际上，您可以使用这种技术使用许多不同的语言，尽管您可能需要一点调整，这取决于您选择的语言。

当然，从 bash 脚本调用另一个程序并不需要做什么特别的事情。毕竟这才是它的主要用途:调用其他程序。然而，将脚本分布在多个文件中并不方便。它们可能会不同步，如果你想把它发送给某人或另一台机器，你必须记住得到什么。最好把所有东西都放在一个文件中。

## 文件都在这里

关键是使用 bash 的经常被遗忘的 here 文档特性。当所讨论的程序是像 Python 这样的解释器时，这样做效果最好。

```

#!/bin/bash
echo Welcome to our shell script

python <<__EOF_PYTHON_SCRIPT
print 'Howdy from Python!'
__EOF_PYTHON_SCRIPT

echo "And we are back!"

```

## 主题变奏曲

当然，任何支持 here 文档的 shell 都可以做到这一点，而不仅仅是 bash。你也可以使用其他翻译。例如:

```

#!/bin/bash
echo Welcome to our shell script

perl <<__EOF_PERL_SCRIPT
print "Howdy from Perl\n"
__EOF_PERL_SCRIPT

echo "And we are back!"

```

这可能会令人困惑，但是您甚至可以用 Python 编写一些部分，用 Perl 或另一种语言编写其他部分。尽量不要忘乎所以。

## 以防万一

在极少数情况下，解释器不会从标准输入中获取解释后的文件。是一个臭名昭著的罪犯。虽然您可以在命令行中嵌入整个脚本，但这可能会很尴尬，并导致引用问题。但是仅仅为了发送给`awk`而写出一个临时文件似乎很傻。幸运的是，你不必这样做。

至少有两种常见的方法来处理这个问题。第一种是使用 bash 流程替换。这基本上是从 subshell 的标准输出中创建一个临时文件:

```

#!/bin/bash
# Hybrid bash/awk Word count program -- totally unnecessary, of course...

echo Counting words for "$@"
awk -f <( cat - <<EOF_AWK

    BEGIN {
        wcount=0;
        lcount=0;
    }

    {
        lcount++;
        wcount+=NF;
    }

    END {
        print "Lines=" lcount;
        print "Words=" wcount;
    }

    EOF_AWK
) "$@"

echo Hope that was enough
exit 0

```

## 另一种方式

还有另一种方法来组织您的进程替换，因此它们都聚集在脚本的末尾，由一个标记(如“AWK _ 开始”和“AWK _ 结束”)或您喜欢的任何其他字符串对包围。想法是将每个伪文件放在脚本末尾它自己的部分。然后，您可以使用任意数量的技术，如`sed`或`awk`来删除这些行，并像以前一样进行处理替换。

有两个小问题。首先，脚本需要在假文件开始之前退出。那很简单。您只需要确保在脚本的结尾编写一个退出代码，这可能是您无论如何都应该做的。另一个问题是搜索标记文本。如果你搜索文件，比如说，AWK_START，你需要确保搜索模式本身没有被找到。您可以通过在搜索字符串中使用一些任意的括号或者分解搜索字符串来解决这个问题。考虑一下这个:

```

#!/bin/bash
# Hybrid bash/awk Word count program -- totally unnecessary, of course...

echo Counting words for "$@"
# use brackets
#awk -f <( sed -e '/[A]WK_START/,/[A]WK_END/!d' $0 ) "$@"
# or
AWK_PREFIX=AWK
awk -f <( sed -e "/${AWK_PREFIX}_START/,/${AWK_PREFIX}_END/!d" $0 ) "$@"

echo Hope that was enough
exit 0

# everything below here will be the supporting "files", in this case, just one for awk

# AWK_START

BEGIN {
    wcount=0;
    lcount=0;
}

{
    lcount++;
    wcount+=NF;
}

END {
    print "Lines=" lcount;
    print "Words=" wcount;
}

#AWK_END

```

没有理由你不能在最后有多个假文件，每一个都有不同的标记对。但是，请注意，标记是发送给程序的，这就是它们作为注释出现的原因。如果这些程序不使用`#`作为注释标记，你需要稍微改变标记行，写一个更复杂的`sed`表达式，或者添加一些命令在发送前去掉第一行和最后一行。

## 那是一个包裹

你可以争辩说，你可以用一种语言做所有你需要做的事情，这几乎肯定是真的。但是在一个文件中嵌入多个文件的技巧可以使创建和分发脚本变得更容易。这有点类似于我们在 Linux Fu 的上一期中如何让[自安装归档文件](https://hackaday.com/2021/04/09/linux-fu-shell-script-file-embedding/)。如果你更喜欢用 C 或 C++ 编写[脚本，你也可以这么做。](https://hackaday.com/2019/09/17/linux-fu-shell-scripts-in-c-c-and-others/)