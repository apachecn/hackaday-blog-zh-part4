# Linux 傅:是陷阱！

> 原文：<https://hackaday.com/2019/08/26/linux-fu-its-a-trap/>

很容易认为像 Bash 这样的 Linux shell 只是在终端输入命令的一种方式。但是，事实上，它也是一种强大的编程语言，正如我们从从 web 服务器到使危险命令更加安全的简单实用程序的项目中看到的那样。然而，像大多数编程语言一样，复杂性也是多层次的。你可以花一点时间勉强度日，或者你可以投入更多的时间来学习这门语言，并希望能写出更健壮的程序。

## 信号

[![](img/b1bee23c09355620a9e79445ef7a6366.png)](https://hackaday.com/wp-content/uploads/2017/01/optimizing-linux-thumbnail.jpg) 如果你在运行一个 Linux 程序，哪怕是一个 shell 脚本，在一定条件下都是要接收信号的。例如，`SIGINT`或信号 2 是当您按下 Control+C 时发生的情况。不过，还有许多其他信号。极少数信号，如信号 9，即`SIGKILL`会终止你的程序，没有问题，你不能停止它。但是其他大部分信号都可以被捕捉到。你要么忽略它们，要么采取行动。

有些信号来自系统。以下是常见信号及其编号的列表。

1- `SIGHUP`(挂机)

2—`SIGINT`(中断；控制+C)

3—`SIGQUIT`(退出)

4—`SIGILL`(非法指令)

9—`SIGKILL`(杀死)

如果您想查看一个长列表，请在命令提示符下尝试使用`trap -l`。我的系统列出了 64 种不同的信号名称。

您可以使用`kill`或`killall`命令向进程发送信号:

```
kill -1 4234
killall -9 emacs
kill -SIGHUP 3152
```

除了标准信号，Bash 还有一些特殊的信号。这里有一个列表，但是您应该查看 trap 下的 [Bash 手册以获得详细信息:](https://www.gnu.org/software/bash/manual/html_node/Bourne-Shell-Builtins.html#index-trap)

*   退出–当 shell 退出时
*   ERR——当错误发生时(具体细节参见 Bash 手册)
*   return–外壳函数或源脚本完成时
*   调试–在每个命令执行之前

## 会发生什么？

[![](img/0e3727f4268dc6bf174cb1815287dacc.png)](https://hackaday.com/wp-content/uploads/2019/08/trap.jpg) 很多时候，当你的程序或者脚本得到一个信号，它就会停止。有一些例外，这取决于其他事情。比如使用 [`nohup`](https://hackaday.com/2017/03/10/linux-fu-keeping-things-running/) 会保护你的程序免受`SIGHUP`的伤害。

在 shell 脚本中，您可以使用 trap 命令来“捕获”一个信号或一系列信号。你有三个选择:

1.  不提供将信号设置为默认处理程序的操作
2.  提供一个空动作(例如“”)来设置程序忽略信号
3.  提供一段代码，在信号出现时运行

例如，要忽略`SIGQUIT`和`SIGHUP`，您可以写:

```
trap "" SIGQUIT SIGHUP
```

或者，如果你不想忽视，你可以写:

```
trap "echo Bye; exit" SIGINT
```

要恢复默认值，请使用:

```
trap SIGINT
```

简单吧？试试这个:

```
#!/bin/bash
trap "echo ; echo Bye ; echo ; exit" SIGINT
while true
do
   sleep 1
done
```

运行它，然后按 Control+C。

## 很简单，但是…

这很简单，但是有一点不方便。如果您用相同的代码捕获多个信号，您没有简单的方法来找出哪个信号导致了陷阱。如果能有一个陷阱函数来服务于一系列不同的陷阱，比如使用 case 或 if 语句来理解哪个信号发生了，那就太好了。

[![](img/5d8c14394425afa78504bbd46b81d390.png)](https://hackaday.com/wp-content/uploads/2019/08/monk.png) 这不是内置的 Bash，但是你只要做一点工作就可以做到。事实上，我写了 [trappist](https://github.com/wd5gnr/trappist) 来为你做这些。它是这样工作的:在脚本中包含`trappist.sh`文件，然后编写一个名为`trappist_trap`的函数。它需要一个参数来告诉你发出了什么信号。如果您不提供，将会有一个哑缺省值，您可以在以后覆盖它。

可以用几种方式调用`trappist_init`。如果您不提供任何参数，那么您可以捕捉的所有信号都将指向您的陷阱函数。如果您愿意，您可以传递一个@作为第一个参数，后跟一个前面带有+或–的信号名称列表。像这样:

```
trappist_init  @ +SIGINT -SIGQUIT -SIGHUP
```

信号的顺序并不重要。这个命令行捕获所有信号，但是使用 SIGINT 的默认处理程序，忽略 SIGQUIT 和 SIGHUP。如果你愿意，也可以省略@符号。

调用`init`函数的另一种方法是使用等号:

```
trappist_init = SIGINT SIGQUIT +SIGHUP -SIGUSR1
```

在这种情况下，只有 SIGINT 和 SIGQUIT 会转到 trap 函数。SIGHUP 将获得默认处理程序，SIGUSR1 将被忽略。

典型的陷阱函数可能如下所示:

```
function trappist_trap()
{
case $1 in
SIGALRM)
TRAP_DOWNCT=3 # After 10 seconds go back to 3
echo ^C reset
;; . . . 

```

## 中间部分

[![](img/b9355155f8f564c09d182e0892e92a02.png)](https://hackaday.com/wp-content/uploads/2018/05/tux2.png) 剧本挺好琢磨的。核心是一个循环，它向系统添加陷阱，一次添加一个，并附加参数。仅有的两件棘手的事情是脚本如何试图检测你的陷阱处理器，而你没有，它使用`eval`为你创建一个简单的函数。

实际的设置变成了:

```
trap "trappist_trap $t" $t
```

这一行接受一个名为 t 的信号，捕获它，并使正确的信号名作为参数传递。之后，就很容易明白事情是如何运作的了。

如果你想一想，这些信号很像中断，尽管其中一些不会立即触发——换句话说，只有少数提到的信号会立即发生。然而，默认情况下，每个“中断”在向量表中都有一个条目。`Trappist`填充表格，将所有内容推送到一个“中断服务程序”

注意，如果有办法让脚本识别出信号，那么`trappist`就没有必要了。你可以写:trap `trappist_trap` `SIGQUIT` `SIGINT` `SIGHUP` …然后你必须找出 trap 函数中的信号。当然，如果你想对所有信号一视同仁，你就不用担心这个问题。

我们已经讨论了在之前[停止挂起的一些细节。我们还看了用](https://hackaday.com/2017/03/10/linux-fu-keeping-things-running/)[二进制文件](https://hackaday.com/2018/06/29/linux-fu-scripting-for-binary-files/)编写脚本。