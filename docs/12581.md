# Linux Fu: Bash 字符串

> 原文：<https://hackaday.com/2022/01/26/linux-fu-bash-strings/>

如果你是一个传统的程序员，使用`bash`编写脚本有时可能会受到限制，但是对于某些任务来说，`bash`可能会非常高效。事实证明，`bash`的一些限制实际上是旧 shells 的限制，人们为了兼容而编码。还有其他问题是因为`bash`中的一些高级功能晦涩难懂或令人困惑。

字符串就是一个很好的例子。你不会认为`bash`是一种字符串操作语言，但它有许多处理字符串的强大方法。事实上，它可能有太多的方式，因为功能会出现在多个地方。当然，您也可以调用程序，有时调用`awk`或 Python 脚本来完成繁重的工作会更容易。

但是让我们坚持使用`bash` -isms 来处理字符串。显然，您可以将一个字符串放入环境变量中，然后再取出来。我假设你知道字符串插值和引用是如何工作的。换句话说，这应该是有意义的:

```

echo "Your path is $PATH and the current directory is ${PWD}"

```

## 多头和空头

假设你想知道一个字符串的长度。这是一个非常基本的字符串操作。在`bash`中，可以写出`${#var}`来求`$var`的长度:

```

#/bin/bash
echo -n "Project Name? "
read PNAME
if (( ${#PNAME} > 16 ))
then
   echo Error: Project name longer than 16 characters
else
   echo ${PNAME} it is!
fi

```

(()形成了一个算术上下文，这就是为什么您可以在这里使用不带引号的大于号。如果你不介意使用`expr`——这是一个外部程序——至少还有两种方法可以实现:

```

echo ${#STR}
expr length "${STR}"
expr match "${STR}" '.*'

```

当然，如果你允许自己在`bash`之外调用，你也可以使用`awk`或其他任何东西来做这件事，但是我们将坚持使用`expr`，因为它相对来说是轻量级的。

## 瑞士军刀

事实上，`expr`除了长度和匹配之外，还可以做很多字符串操作。您可以使用`substr`从字符串中提取子字符串。首先使用`index`来查找字符串中的特定字符通常很方便。`expr`程序使用 1 作为字符串的第一个字符。比如说:

```

#/bin/bash
echo -n "Full path? "
read FFN
LAST_SLASH=0
SLASH=$( expr index "$FFN" / ) # find first slash
while (( $SLASH != 0 ))
do
   let LAST_SLASH=$LAST_SLASH+$SLASH  # point at next slash
   SLASH=$(expr index "${FFN:$LAST_SLASH}" / )  # look for another
done
# now LAST_SLASH points to last slash
echo -n "Directory: "
expr substr "$FFN" 1 $LAST_SLASH
echo -or-
echo ${FFN:0:$LAST_SLASH}
# Yes, I know about dirname but this is an example

```

输入一个完整的路径(如`/foo/bar/hackaday`)，脚本会找到最后一个斜杠，并使用两种不同的方法打印出名称，直到最后一个斜杠。这个脚本利用了`expr`，但是也使用了`bash`的内置子串提取语法，从索引零开始提取。例如，如果变量 FOO 包含“Hackaday”:

*   ${FOO} -黑客攻击
*   ${FOO:1} ->
*   $ { FOO:5:3 }-->天

第一个数字是偏移量，如果是正数，第二个数字是长度。您也可以使这两个数字中的任何一个为负，尽管如果偏移量为负，则冒号后需要一个空格。例如，字符串的最后一个字符位于索引-1 处。负长度是从字符串末尾开始的绝对位置的简写。所以:

*   $ { FOO:-3 }-->天
*   $ { FOO:1:-4 }-->确认
*   $ { FOO:-8:-4 }-->黑客

当然，正如您在示例中看到的，这两个数字中的一个或两个都可能是变量。

## 少即是多

有时候你不是想找到什么，只是想摆脱它。`bash`使用固定字符串或基于全局的模式匹配，有很多方法来删除子字符串。有四种变化。一对删除从字符串的前面删除最长和最短的可能子字符串，另一对从字符串的后面做同样的事情。考虑一下这个:

```

TSTR=my.first.file.txt
echo ${TSTR%.*} # prints my.first.file
echo ${TSTR%%.*}  # prints my
echo ${TSTR#*fi}  # prints rst.file.txt
echo $TSTR##*fi} # prints le.txt

```

## 转换

当然，有时候你不想删除，就像你想用一个字符串替换另一个字符串一样。您可以使用一个斜杠替换搜索字符串的第一个实例，或者使用两个斜杠进行全局替换。你也可以不提供替换字符串，你会得到另一种方法来删除字符串的一部分。另一个技巧是添加#或%将匹配锚定到字符串的开头或结尾，就像删除一样。

```

TSTR=my.first.file.txt
echo ${TSTR/fi/Fi}   # my.First.file.txt
echo ${TSTR//fi/Fi}  # my.First.File.txt
echo ${TSTR/#*./PREFIX-} # PREFIX-txt  (note: always longest match)
echo ${TSTR/%.*/.backup}  # my.backup (note: always longest match)

```

## 多方面的

在`bash`中操作字符串的一些更常见的方法与处理参数有关。假设您有一个脚本，它期望设置一个名为`OTERM`的变量，但是您希望确保:

```

REALTERM=${OTERM:-vt100}

```

如果在`OTERM`中没有任何内容，那么`REALTERM`将具有`OTERM`的值或字符串“vt100”。有时你想设置`OTERM`本身，这样当你可以分配给`OTERM`而不是`REALTERM`时，有一个更简单的方法。使用:=代替:-序列。如果你这样做了，你根本不需要赋值，尽管如果你喜欢你可以使用一个:

```

echo ${OTERM:=vt100}  # now OTERM is vt100 if it was empty before

```

您也可以反过来，只在主值不为空时替换该值，尽管这通常不太有用:

```

echo ${DEBUG:+"Debug mode is ON"}  # reverse -; no assignment

```

一种更极端的方法是将错误消息打印到 stderr 并中止非交互式 shell:

```

REALTERM=${OTERM:?"Error. Please set OTERM before calling this script"}

```

## 以防万一

将东西转换成大写或小写相当简单。您可以提供匹配单个字符的 glob 模式。如果你省略它，它和？，它匹配任何字符。您可以选择更改所有匹配的字符，或者只尝试匹配第一个字符。以下是必举的例子:

```

NAME="joe Hackaday"

echo ${NAME^} # prints Joe Hackaday (first match of any character)
echo ${NAME^^} # prints JOE HACKADAY (all of any character)
echo ${NAME^^[a]} # prints joe HAckAdAy (all a characters)
echo ${NAME,,] # prints joe hackaday (all characters)
echo ${NAME,] # prints joe Hackaday (first character matched and didn't convert)
NAME="Joe Hackaday"
echo ${NAME,,[A-H]} # prints Joe hackaday (apply pattern to all characters and convert A-H to lowercase)

```

最近版本的`bash`也可以使用`${VAR@U}`和`${VAR@L}`转换大写和小写，以及使用`@u`和`@l`转换第一个字符，但是你的里程可能会有所不同。

## 试验合格

你可能意识到当你做一个标准测试时，实际上调用了一个程序:

```

if [ $f -eq 0 ]
then ...

```

如果您在`/usr/bin`上执行 ls，您将看到一个名为“[”的可执行文件，作为测试程序的简写。然而，`bash`有两个括号形式的自己的测试:

```

if [[ $f == 0 ]]
then ...

```

这个内置测试可以使用=~来处理正则表达式，所以这是匹配字符串的另一个选项:

```

if [[ "$NAME" =~ [hH]a.k ]] ...

```

## 明智地选择

当然，如果你正在做大量的文本处理，也许你不需要使用`bash`。即使你是，不要忘了你总是可以利用其他程序，如 tr、`awk`、`sed`和许多其他程序来做这样的事情。当然，性能可能不会那么好，但是如果你担心性能，为什么还要写脚本呢？

除非你发誓不再使用脚本，否则在你的口袋里放一些这样的技巧是很好的。明智地使用它们。