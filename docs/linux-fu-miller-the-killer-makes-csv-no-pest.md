# Linux 富:米勒黑仔使 CSV 没有害虫

> 原文：<https://hackaday.com/2022/12/28/linux-fu-miller-the-killer-makes-csv-no-pest/>

从历史上看，Unix 和 Linux 的一个优点是一切都是文件，而文件只是字符序列。当然，现代的做法是，一切都不是一个文件，有一些强加的结构的文件激增。然而，如果您曾经在文件访问是按块进行的旧系统上工作过，您会喜欢类似 Unix 的文件。像`awk`、`sed`和`grep`这样的经典工具都是基于这个想法工作的。文件只是字符。但这有时也有问题。这就是名为[米勒](https://github.com/johnkerl/miller)的工具背后的动机，我认为它值得更多的关注，因为对于某些任务来说，它是一个救生员。

## 问题是

考虑尝试处理一个逗号分隔的文件，称为 CSV 文件。这种类型的文件有很多种。这里有一个定义了两个“列”我特意使用了不同的行格式作为测试，但大多数情况下，整个文件只有一种格式:

```
Slot,String 
A,"Hello" 
"B",Howdy 
"C","Hello Hackaday" 
"D","""Madam, I'm Adam,"" he said." 
E 100,With some spaces!
X,"With a comma, or two, even"
```

 第一列，槽，具有项目 A、B、C、D 和 E 100。请注意，有些项目是引用的，但其他的没有。无论如何，列内容是 B 而不是“B ”,因为引号不是数据的一部分。

第二列 String 混合了引号、无引号、空格，甚至引号中的逗号。假设您想用`awk`来处理这个。可以做，但是很痛苦。注意，引号使用双引号进行转义，这是 CSV 文件中的习惯。编写一个正则表达式来打破这种局面并非不可能，但却很痛苦。这就是米勒的切入点。它知道 CSV、JSON、KDVP8 和其他一些数据格式。它还可以输出这些格式和其他格式，比如 Markdown。

## 简单的运行示例

因为它知道格式，所以可以方便地处理文件:

$ MLR–icsv cat miller . in
Slot = A，String=Hello
Slot=B，String=Howdy
Slot=C，String=Hello Hackaday
Slot=D，String="Madam，我是亚当，"他说。
Slot=E 100，String =带一些空格！
Slot=X，String =带逗号，或两个，偶数

[![](img/0f8b7c985335c25680b2c928b619c33f.png)](https://hackaday.com/wp-content/uploads/2022/12/miller1.png) 注意到没有命令叫“米勒”命令名为“mlr”这个输出对于用`awk`进一步处理来说是一个不错的格式，但是我们不必这样做。米勒也许能做我们需要的一切。不过，在我们看到这一点之前，考虑一下如果您只是想要一个漂亮的格式输出会发生什么:

不算太差！别忘了，这个工具对 JSON 和其他格式也会有同样的效果。

## 这么多选择

选择的数量令人望而生畏。有传递或忽略注释、处理压缩数据或稍微定制输入或输出文件格式的选项。

但是对米勒来说真正的力量是动词。在上面的例子中，动词是`cat`。这些命令大多以它们复制的 Linux 命令命名。例如，`cut`将从数据中删除某些字段。`grep`、`head`和`tail`命令都会按照您的预期执行。

也有许多新动词。`Count`会给你一个已经过去了多少数据的计数，`filter`是`grep`的一个更好的版本。您可以进行类似数据库的连接、排序，甚至统计，并生成基于文本的条形图。

`filter`和`put`命令为[提供了一个完整的编程语言](https://miller.readthedocs.io/en/latest/reference-dsl-builtin-functions/index.html)，它拥有你期望在像`awk`或`Perl`这样的语言中找到的所有东西。

好的是，当你想删除一个字段或排序时，你可以通过名字来引用它(比如“Slot”)，米勒会知道你的意思。如果必须的话，有一种方法可以引用带有数字的字段，但这在米勒脚本中很少见。

例如，如果您想要删除一些带有“库存”和“储备”字段的数据，您可以编写如下内容:

`mlr --icsv --opprint cut -f stock,reserve inventory.csv`

或者，您可能希望选择库存为“N”的行:

```
mlr --icsv --opprint filter '$stock == "N"' inventory.csv
```

## 去看书吧

这里没有足够的空间来涵盖这个强大程序的所有功能。我建议你在 10 分钟后去看看[米勒，这是官方文件的一部分。您仍然需要进一步阅读文档，但至少您将有一个良好的开端。](https://miller.readthedocs.io/en/latest/10min/)

别误会，我们还是喜欢 [awk](https://hackaday.com/2016/06/21/gawking-text-files/) 。只要做一点工作，你就可以让它做[几乎任何事情](https://hackaday.com/2020/09/29/linux-fu-making-awk-a-bit-easier/)。但如果能和米勒少干点活，何乐而不为呢？