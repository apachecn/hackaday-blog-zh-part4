# Linux Fu:控制终端

> 原文：<https://hackaday.com/2018/11/28/linux-fu-controlling-the-terminal/>

Linux 终端比过去的电传打字机有更多的功能。在电传打字机上，文字喷涌而出，向上滚动，然后永远消失。一个真正的终端可以使用转义符来导航和模拟你喜欢的 GUI。然而，在最底层这样做是一件苦差事，并且限制了可移植性。幸运的是，所有的艰苦工作都已经完成了。

首先，有一个大型的终端功能数据库可供您使用:`terminfo`。此外，还有一个名为`curses`或`ncurses`的高级库，它简化了编写控制终端显示的程序。深入挖掘`ncurses`的每个角落可能需要数年时间。取而代之的是，我将讨论如何使用`ncurses`附带的一个名为`tput`的程序来控制终端。使用这两个命令，您可以弄清楚您正在处理哪种终端，然后随心所欲地操纵它。我们开始吧！

## 关于 terminfo

你要问的最根本的问题是你在和什么样的终端对话。答案就在`$TERM`环境变量中，如果您要求您的 shell 打印该变量，您将看到它认为您正在使用的是什么:`echo $TERM`。
例如，常见的类型是 vt100 或 linux 控制台。这通常是由系统设置的，除非你有充分的理由，否则你不应该改变它。当然，从理论上讲，您可以手动处理这些信息，但是如果必须找出所有的方法来做一些事情，比如在 Linux 能够理解的许多终端上清除屏幕，那将是令人畏惧的。

这就是为什么会有 terminfo 数据库。在我的系统中，`/lib/terminfo`(不包括目录)中有 43 个文件，分别用于名称为`dumb`、`cygwin`、`ansi`、`sun`和`xterm`的终端。查看文件不是很有用，因为它们是二进制格式的，但是`infocmp`程序可以逆转编译过程。下面是运行`infocmp`并询问`vt100`的定义的部分结果:

```

vt100|vt100-am|dec vt100 (w/advanced video),

       am, mc5i, msgr, xenl, xon,

        cols#80, it#8, lines#24, vt#3,

        acsc=``aaffggjjkkllmmnnooppqqrrssttuuvvwwxxyyzz{{||}}~~,

        bel=^G, blink=\E[5m$&lt;2&gt;, bold=\E[1m$&lt;2&gt;,

        clear=\E[H\E[J$&lt;50&gt;, cr=\r, csr=\E[%i%p1%d;%p2%dr,

```

这可能比二进制版本好不了多少。但你可能会猜到，它在某种程度上告诉你，贝尔的角色是 Control-G (^G).您可能还会猜测\E 是一个转义字符，并想不出如何将字符加粗或清空屏幕。有些数据是结构化的，例如 24 行 80 列的输出。这些功能(比如使用 xon/XOFF 协议的 XON)不查一下就很难搞清楚。

然而，确切的含义并不重要。因为我们将使用更高级别的构造来告诉`tput`我们想要什么，它——或者至少是`ncurses`库——将在`terminfo`中查找数据，然后做正确的事情。

## 使用 tput 获取信息

我不确定这个名字`tput`来自哪里——你必须假设它是“终端投放”但是您也可以使用`tput`来获取信息。例如，你可以说`tput longname`，而不是看着`$TERM`。你也可以学习其他的东西。例如，终端有多宽(以字符为单位)？`tput cols`。

这对于可能改变尺寸的 X 窗口下的终端来说尤其方便。在脚本中，您可以捕获`WINCH`事件，以便在终端调整大小时运行一些代码，这非常方便。其他你能读到的是行数和颜色数。

[![](img/865a91000f32ddb490ff5745c166ed28.png)](https://hackaday.com/wp-content/uploads/2018/11/first.png)

例如，假设你已经安装了`fortune`，你可能想要一个每 30 秒更新一次的财富窗口。这将是很好的，虽然有财富中心，即使屏幕改变大小。

```
#!/bin/bash
# Simple centered fortune
TIMEOUT=30

do_print() {
  w=$(tput cols)
  h=$(tput lines)
  n=${#text}
  spaces=$(( ($w-$n)/2 ))
  lines=$(( $h/2 ))
  clear
  for I in `seq 1 $lines`
  do
   echo 
  done
  for I in `seq 1 $spaces`
  do
    echo -n ' '
  done
  echo $text
}

while true
do
  text=$(fortune -n $(tput cols) -s )
  do_print
  sleep ${TIMEOUT:-30}
done
```

这工作得很好。当一笔财富出现时，它会出现在窗户的中央。我在`do_print`中画所有的图，因为我对那个功能有未来的计划。

`fortune`命令告诉它只给我们短的运气，短的定义是根据`tput`的屏幕宽度。我在这里使用了一些特定于 bash 的技术，包括表达式求值、字符串长度`(${#text})`和默认参数

不过，你会注意到，如果你调整窗口的大小，在新的出现之前，财富不会在正确的位置。我们如何解决这个问题？

## 使用绞盘

结果，当终端调整大小时，程序应该得到一个`SIGWINCH`信号。我说“应该”是因为有些情况下不会发生这种情况，例如在一些 emacs shells 中。(事实上，在 emacs 中，很多都是这样。)可能还有其他的设置也会有问题。但是，假设代码得到了`SIGWINCH`，就很容易处理了。这行代码应该会处理好:`trap do_print WINCH`

唯一的问题是，它不适合这个脚本。脚本大部分时间都在休眠，只有当它醒来时才会收到信号。但到了那个时候，你也会得到一笔新的财富，所以当它做正确的事情时，它要么用新的财富做，要么用旧的财富做，并立即被覆盖。

答案是少睡觉。然而，对于系统的其余部分来说，简单地坐着旋转是不礼貌的，所以我将睡眠更改为:

```
# Can't just sleep for timeout
# because we won't get SIGWINCH when sleeping
# If you want faster response, sleep less
TO=${TIMEOUT:-30}
TO=$(( $TO * 2 ))
for I in `seq 1 ${TO}`
do
   sleep 0.5
done
```

这有点复杂，因为我想睡 500 毫秒，而不是一整秒。你睡得越少，剧本对变化的反应就越快。但是，你浪费的系统资源越多，所以这是一个权衡。

## 格式化

了解屏幕的大小非常有用。但是您也可以使用`tput`来格式化文本:

*   闪烁–闪烁文本
*   粗体–粗体文本
*   invis–不可见的文本
*   rev–反向视频
*   rms 0–结束突出模式
*   rmul–结束带下划线的文本
*   setab–背景颜色
*   setaf-前景色
*   SG r0–关闭所有属性
*   smso–启动杰出模式
*   smul–开始下划线模式

颜色取值范围从 0 黑色到 7 白色。值为 9 会重置默认颜色。尝试更改`echo $text`行，如下所示:

```
tput setab 7   # white background
tput setaf 4   # blue text
tput bold
echo $text
tput sgr0
```

[![](img/878008520576008d5a090aeaa9e24faa.png)](https://hackaday.com/wp-content/uploads/2018/11/last.png)

遗憾的是，除非自己定义，否则不能使用颜色名称。如果你不喜欢对每个项目使用单独的`tput`调用，你可以使用`-S`选项和一个`here`文档:

```
tput -S &lt;&lt; tputEOF
  setab  7  # white
  setaf  3  # blue
  bold
tputEOF
```

尽管如此，您仍然需要每行放置一个项目。我不能说为什么突出和下划线模式有一个特定的结束代码，其余的你只需要使用`sgr0`来关闭一切。

## 擦除和保存

我使用了`clear`来清空屏幕，但我也可以使用`tput clear`。事实上，在某些系统上，`clear`是`tput`的别名，程序足够聪明，知道如果你用`clear`调用它，它应该清除屏幕并退出。

有几个命令可以让您清除屏幕的某些部分，或者保存和调用屏幕:

*   清除–清除整个屏幕
*   ed–清除至屏幕末端
*   El–清除至行尾
*   el1–清除至行首
*   RM cup–恢复保存的屏幕
*   sm cup–保存屏幕并清除

如果你想看到它工作，你可以从命令行尝试`tput smcup`。只需发出命令，做一些事情，然后发出`tput rmcup`。如果您想给整个屏幕着色，请在 fortune 脚本中尝试这样做，替换 clear 命令:

```
tput setab 2
tput clear
```

然后再向下取出`setab`命令。

[![](img/7fd06ec65157d6e29bfa8eea11a681e4.png)](https://hackaday.com/wp-content/uploads/2018/11/backgr.png)

## 光标控制

最后一项是能够在程序控制下移动光标:

*   civis–设置光标不可见
*   cnorm–设置正常光标
*   cud 1–下移一行
*   杯子–设置行和列
*   cuu 1–将光标上移一行
*   主页–将光标移动到左上角
*   RC–恢复保存的光标位置
*   sc–保存光标位置

您现在可以对脚本做得更好，将 do_print 中的两个 for 循环替换为:`tput cup $lines $spaces`，将打印位置定位到正确的位置。

## 其他想法

使用`tput`你可以轻松地创建进度条或逐页显示数据，而不需要依赖外部分页程序。当然，如果你需要一些过于花哨的东西，你可能应该使用 GUI 程序或对话框库。当然，对于 Linux 来说还有很多这样的:`dialog`、`cdialog`、`zenity`、`kdialog`、 [easybashgui](https://github.com/BashGui/easybashgui) 浮现在脑海中。

但是有时候你不能，不想，或者只是不需要涉及更复杂的库。对于简单地将文本放在屏幕上的某个地方，很难超越`tput`。