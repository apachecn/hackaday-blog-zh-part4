# 奇怪的计算机语言:黑客领域指南

> 原文：<https://hackaday.com/2022/01/26/strange-computer-languages-a-hackers-field-guide/>

当你能买到收音机或钟表时，我们为什么要制造它们？为什么我们让 led 毫无目的地闪烁？为什么我们试图从显卡中挤出一个额外的帧？我们不知道为什么，但我们知道。这可能是大多数人在学习 esolang——深奥的编程语言——时的态度，我们不知道为什么人们会创建或使用它们，但他们确实会这样做。

我们不是在谈论那些让人们讨厌的主流语言，比如 Lisp、Forth 或 VBA。我们不是在谈论像 APL 或 Prolog 这样在今天看起来晦涩难懂的老语言。我们谈论的是被制造成…嗯…奇怪的语言。

## 插入

我们必须从头开始。插入。这是 1972 年作为一个笑话开始的，这个缩写据称是编译器语言，没有可发音的缩写。然而，直到 1990 年左右才真正实施。现在有两个:C-interc 和 CLC-interc。

由于 INTERCAL 是一个模仿，它做出了一些非常奇怪的选择。例如，按位运算符像 AND 一样使用两个参数进行运算，但其中一个参数是相反的。也就是说，一个操作数的高位与第二个操作数的低位相匹配。为了向社会习俗致敬，有一个修饰语叫做 PLEASE，你有时应该使用它，例如，在“PLEASE READ IN”中读取数据如果你不经常使用它，编译会失败，警告你程序不够礼貌。然而，如果你太频繁地使用它，你也会得到一个你的程序过分礼貌的错误。

最初，实现使用了 EBCDIC，所以它使用了一些在传统的 7 位 ASCII 系统上没有出现的字符。这迫使一些字符替换，现在，有了 Unicode，一些版本将允许旧风格的字符，如果你喜欢他们。INTERCAL 手册重新命名了几乎所有的特殊字符，以免混淆。单引号是“火花”，等号是“半网”。只有&符号没有受到影响。

想了解更多？小心[你对](http://catb.org/~esr/intercal/)的愿望。

## 虚假和愚蠢的

[![](img/7badcf1657f1dc2b835ac306475b9383.png)](https://hackaday.com/wp-content/uploads/2022/01/confused.jpg) 快进到 1993 年，虚假的诞生，一叠语言让人读不懂。值得安慰的是，编译器只需要 1，024 字节。这启发了一种更简单的语言，Brainf**k。一个 BF 程序只需要八个字符。

Brainf**k 已经产生了许多类似的语言，如 Befunge 和 JSF**k。如果你在这篇文章中只听说过一种语言，那很可能就是这种。

它看起来像什么？来自[深奥语言维基](https://esolangs.org/wiki/Brainfuck):

```
++++++++[>++++[>++>+++>+++>+<<<<-]>+>+>->>+[<]<-]>>.>---.+++++++..+++.>>.<-.<.+++.------.--------.>>+.>++.
```

顺便说一句，那是你好世界！

## 二元组合逻辑和 Unlambda

我们曾经认识一位大学教授，他常说“最大化布尔变量”，其实他的意思是“将位设置为 1”。我们认为他会喜欢 BCL。如果你想用 BCL 表达 true，你就写 K(KK)。假的？K(K(SK))。从那以后情况会变得更糟。下面是 XOR:S(S(S(SS)(S(S(SK))S))k。

然而，这是二进制的，所以 S 实际上是 01，K 是 00，左括号是一个 1。超级奇怪，显然在一些理论数学研究中有一些应用。

这有几个版本，都略有不同。[比如 Unlambda](https://esolangs.org/wiki/Unlambda) ，就用了很多不同的字符。这是 Unlambda 中的一个“猫”程序:

```
```s`d`@|i`ci
```

## 空白

大多数编程语言不关心空白，你可以随意使用它，也可以不使用。也就是说，在 C 语言中，您可以编写:

x = 10 * 2；

或者:

x = 10

*

2;

编译器不在乎。Python 不一样。压痕等级很重要。空白将这一点发挥到了极致。整个程序是用制表符、空格和换行符编写的，所有内容都被忽略。这可能看起来很奇怪，但有趣的是它允许你将一个程序隐藏在另一个程序中——只要它不是 Python 程序。

第一个空白字符告诉你下一个是什么意思。例如，所有的流控制序列都以换行开始。堆栈操作以空格开始。制表符和换行符引入了 I/O 操作。一个选项卡和一个空格用于数学，两个选项卡用于管理堆访问。

偶数是二进制的，空格为正，制表符为负。之后，空格为 0，制表符为 1。

## LOLCODE

虽然空白可能比 Brainf**k 更难理解，但一些语言试图模仿特定的可读事物。一个很好的例子:LOLCODE 拥有与 LOLCAT meme 标题相匹配的程序。显然，毕竟，笑猫是互联网发明的主要原因。

为什么我们认为猫会这样说话？我们不确定，但我们有一种感觉，真正的猫的大脑内部的叙述更像是，“现在很难找到好的仆人！”古埃及人崇拜猫，猫也没有忘记这一点。

这是一个数到 10 的程序:

```
HAI 1.3
IM IN YR loop UPPIN YR var TIL BOTH SAEM var AN 10
VISIBLE SMOOSH var AN " " MKAY!
IM OUTTA YR loop
KTHXBYE
```

## 摇滚明星

[![](img/c4428c4e5e56ccd64bb1e8a39b52ef16.png)](https://hackaday.com/wp-content/uploads/2022/01/rockstar.jpg) 也许你不是 LOLCATs 的粉丝，但你喜欢摇滚乐。那么，Rockstar 就是适合你的编程语言。变量名几乎可以是任何东西，数据有类似“神秘”的类型

我们认为，要成为一名优秀的这种语言的编码者，你需要留长发，说话含糊不清，并拥有至少一件由氨纶制成的衣服。仔细想想，这描述了我们认识的相当多的程序员。

在它所做的聪明的事情中，数字用单词的长度来表示，许多编程结构有“明显的”英语语言关联。所以《恨是水》给变量“恨”赋值 5。

下面是 Fizbuzz 写于 [Rockstar](https://codewithrockstar.com/online) :

```
Midnight takes your heart and your soul
While your heart is as high as your soul
Put your heart without your soul into your heart

Give back your heart

Desire is a lovestruck ladykiller
My world is nothing 
Fire is ice
Hate is water
Until my world is Desire,
Build my world up
If Midnight taking my world, Fire is nothing and Midnight taking my world, Hate is nothing
Shout "FizzBuzz!"
Take it to the top

If Midnight taking my world, Fire is nothing
Shout "Fizz!"
Take it to the top

If Midnight taking my world, Hate is nothing
Say "Buzz!"
Take it to the top

Whisper my world
```

## 莎士比亚

如果摇滚乐对你来说太单调，总有 SPL，莎士比亚的编程语言。像吟游诗人一样，这种编程语言并不以其简洁著称。

在 SPL，数字尤其棘手。名词有-1 或 1 的值，取决于它们有多好(例如，树和花是 1，而猪是-1)。形容词乘以 2。所以“说谎愚蠢无父大臭半蠢懦夫”是-1(懦夫)* 2 * 2 * 2 * 2 * 2 = -64。

围绕 Hackaday watercooler，我们已经考虑编写这种语言的新版本，其中所有程序都是以吟游诗人和弗朗西斯·培根爵士之间的对话形式出现的。我们称之为摇烤。

这只是 89 行 [Hello World 脚本](http://shakespearelang.sourceforge.net/report/shakespeare/#sec:hello) —呃—程序的一部分:

```
The Infamous Hello World Program.

Romeo, a young man with a remarkable patience.
Juliet, a likewise young woman of remarkable grace.
Ophelia, a remarkable woman much in dispute with Hamlet.
Hamlet, the flatterer of Andersen Insulting A/S.

Act I: Hamlet's insults and flattery.

Scene I: The insulting of Romeo.

[Enter Hamlet and Romeo]

Hamlet:
You lying stupid fatherless big smelly half-witted coward!
You are as stupid as the difference between a handsome rich brave
hero and thyself! Speak your mind!

You are as brave as the sum of your fat little stuffed misused dusty
old rotten codpiece and a beautiful fair warm peaceful sunny summer's
day. You are as healthy as the difference between the sum of the
sweetest reddest rose and my father and yourself! Speak your mind!

You are as cowardly as the sum of yourself and the difference
between a big mighty proud kingdom and a horse. Speak your mind.

Speak your mind!

[Exit Romeo]

Scene II: The praising of Juliet.

[Enter Juliet]

Hamlet:
Thou art as sweet as the sum of the sum of Romeo and his horse and his
black cat! Speak thy mind!
```

## 马尔堡女校

[![](img/0a9659ee00db5c02029e5087c6e686a5.png) ](https://hackaday.com/wp-content/uploads/2022/01/angrydev.jpg) [马尔博尔格](https://esolangs.org/wiki/Malbolge_programming)被设计成难以使用。据报道，第一个打印 hello world 的程序需要另一个计算机程序搜索所有可能的程序，直到找到正确的序列。如果你不认识这个参考，Malbolge 是 Malebolge 的拼写错误，Malebolge 是但丁*地狱*中地狱的第八层。

Malbolge 使用基数为 3 的虚拟机。只有几条指令，包括向右旋转和“疯狂”的操作，这种操作以表格中定义的方式改变位，据我们所知，与任何正常的数学运算无关，本质上是加密。马尔博尔格是如此可怕，以至于有些人试图让自己“稍微不那么邪恶”

## 饶舌的人

[![](img/d05b88414ba6834c72e2cf526f8e5057.png)](https://hackaday.com/wp-content/uploads/2022/01/piet.jpg) 你有没有注意到在科幻电影中，外星人几乎总是用某种我们能听到的声音进行交流？他们要么说英语，要么说一些听起来像安迪·考夫曼扮演角色的话。你很少看到闪着光、发出信息素或发射低频无线电波进行交流的外星人。这个列表中的所有语言都使用某种字符，如数字、符号或单词。[除了皮埃特](https://hackaday.com/2020/01/03/a-programming-language-that-lets-you-code-with-pixels/)。皮埃特程序是皮埃特·蒙德里安创造的那种抽象艺术。

[![](img/01ef2b6edf63c594da50b050a19bec12.png)](https://hackaday.com/wp-content/uploads/2022/01/Piet_Hello_World.gif) 一个单一的码单位是一个码元，多个码元具有相同的颜色。当然，“程序计数器”可以在二维空间移动。例如，如果皮埃特把红色解释为加法，绿色解释为跳跃，那么这将是另一种形式的符号。但事情不是这样的。相反，解释者看的是颜色之间色调和强度的变化。所以色相的一步和明度的不变是加法运算。但是如果颜色变暗了，那就是减法。这里是皮特的 hello world。不要让我们解释！

## 为什么？为什么？

人们为什么创造或使用这些语言是不值得去思考的。为什么有人会买宠物石？人们为什么收集邮票？他们就是这样。尽管如此，学习一点这些古怪的语言可以让你走出舒适区，这并不总是一件坏事。此外，许多人会说为 PIC 或 AVR 编写汇编只是比 Malbolge 稍微不那么神秘，许多黑客读者也这么认为。

至于我们，我们将坚持使用更实用的编程语言。第四个看起来很神秘，但是很棒，可以在专家的手中创建非常清晰的程序。然而，我们确实偶尔会为了好玩而钻研[这些语言](https://hackaday.com/2018/07/28/become-the-rockstar-developer-youve-always-dreamed-of-being/)。