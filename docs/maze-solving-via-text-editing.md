# 通过文本编辑解决迷宫

> 原文：<https://hackaday.com/2020/01/12/maze-solving-via-text-editing/>

Linux 脚本编写人员通常都知道 sed——流编辑器。它的工作很简单:在文本从输入到输出的过程中转换文本。所以如果你想解决一个迷宫，这不会是你想用的工具，对吗？如果你是[xsot]，[你会不同意](https://devpost.com/software/sed-pathfinder)。

你用空格做空白，用#做墙来建造一个迷宫。有一个 S 标记开始位置，一个 E 标记结束位置。当然，迷宫也可以包含换行符。sed 脚本出色地解决了这个问题。

正如作者指出的:

> 主要困难在于缺少常规编程语言通常提供的功能，例如:
> 
> *   算术
> *   字符串以外的数据类型
> *   超过 2 个“变量”
> 
> 此外，sed 正则表达式缺少其他正则表达式系统中存在的特性，如 PCRE(非贪婪匹配、前瞻等)。

我们将承认，我们没有将整个 [122 行脚本](https://gist.github.com/xsot/99a8a4304660916455ba2c2c774e623a)拆开来理解它，但它看起来像是用与从结束到开始的方向相关的特殊标记字符替换了空格。字母 U、D、L 和 R 表示方向。然后，它能够选择最接近的字符，并用箭头(嗯，一个字母 v，一个插入符号，以及小于和大于符号)替换它们。

我们认为这是一种非常不寻常的使用 sed 的方法。输出甚至是彩色和动画。太神奇了。

我们不能说我们曾经用一个脚本命令做过如此奇怪的事情。如果你想复习的话，我们已经看了很多遍[脚本](https://hackaday.com/2019/12/30/linux-fu-leaning-down-with-exec/)。可能最接近的方法是使用 bash 脚本来处理[二进制文件](https://hackaday.com/2018/06/29/linux-fu-scripting-for-binary-files/)。