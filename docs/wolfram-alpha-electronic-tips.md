# Wolfram Alpha 电子提示

> 原文：<https://hackaday.com/2018/08/01/wolfram-alpha-electronic-tips/>

电子学需要很多数学知识。一旦你掌握了所有的代数和微积分，有时走过场是一种拖累。它也容易出错。但是现在，你有了 Wolfram Alpha，它会帮你完成所有的工作，而且非常容易。当我懒得用手解方程或做积分时，我总是用它。但你知道它实际上有一些专门针对电子产品的功能吗？

如果你想在电子或几乎任何技术领域做很多事情，你必须学习一些数学，你不应该仅仅依靠像 Wolfram 这样的工具来回避理解数学。不幸的是，学校经常教导我们，数学的意义在于得到正确的答案。对于簿记员和工程的最后阶段，这可能是真的。但是对工程师和科学家来说，数学的真正价值是培养对事物的直觉。如果你增加一个电容器的值，它的电抗会上升还是下降？负载电阻的一点点变化对功耗的影响是相应的小变化还是大很多？所以你应该明白为什么数学会起作用。但是一旦你这样做了，使用像 Wolfram 这样的工具可以让你把注意力从抽象的问题上解放出来，而不是详细的“繁重的工作”

## 技巧 1:人格分裂

Wolfram 似乎无法决定它是一个符号数学程序还是一个搜索引擎。有时候，仅仅输入一个主题名称就可以得出一些有趣的计算结果。例如，看看当你输入单词 [opamp](https://www.wolframalpha.com/input/?i=opamp) : 时会发生什么

[![](img/a7a82c601fb8d2ba3edba394b98ab02f.png)](https://hackaday.com/wp-content/uploads/2018/07/wolfopamp.gif)

你可以选择多种不同类型的运算放大器电路，以及如何分析它们。Wolfram 非常擅长挑选像 mV 这样的毫伏后缀，尽管我们已经发现了一些阻碍它的后缀(见技巧 2)。你可能感兴趣的其他主题是并联或串联 RLC 电路的各种组合，例如“串联 LC 电路”。输入“[欧姆定律](https://www.wolframalpha.com/input/?i=Ohm%27s+law)告诉你乔治欧姆，但是输入“[欧姆定律计算器](https://www.wolframalpha.com/input/?i=Ohm%27s+law+calculator)更实用一点。但是，如果您忘记了，您可以随时单击公式链接:

[![](img/d8a5d98b05e7d365f6b9b31a8a908d53.png)](https://hackaday.com/wp-content/uploads/2018/07/wolfohm.png)

试试“[巴特沃斯滤波器](https://www.wolframalpha.com/input/?i=butterworth+filter)或者“[切比雪夫滤波器](https://www.wolframalpha.com/input/?i=Chebyshev+filter)”不幸的是，“Sallen-key 滤波器”或“椭圆滤波器”没有任何用处。

## 技巧 2:快速计算

你可以经常给网站一个关键字和一些参数，它会整理出来。例如，如果您需要[一个电容在 4 MHz 下与 100 uH 电感谐振](https://www.wolframalpha.com/input/?i=resonant+frequency+4+MHz+100uH):

[![](img/accd1a0b73961b67d8dbccf9f876108f.png)](https://hackaday.com/wp-content/uploads/2018/07/wolfres.png)

唯一的问题是，有时它会混淆单位。例如，在 Wolfram 中尝试[使用皮法是不划算的:](https://www.wolframalpha.com/input/?i=resonant+frequency+30+pf+100+uH)

[![](img/75e3a4ae37d41cbbea795809d4c21091.png)](https://hackaday.com/wp-content/uploads/2018/07/wolfpf.png) 你总是可以用不同的单位来表示，或者——奇怪的是——如果你[把 100 uH 放在第一个](https://www.wolframalpha.com/input/?i=resonant+frequency+100+uH+30pF)里，它会正确地计算出皮法。

> 更新:正如评论中提到的，混淆的原因是它区分大小写，正确的条目是 pF。第二个例子不是因为顺序，而是因为我在那个例子中随机地大写了 F。现在谁每两周使用 pf 可能是另一天的另一个问题。

## 提示#3:颜色代码

你真的应该学习电阻颜色代码。有很多句子可以帮助你记忆，比如“大男孩赛跑…”或“坏啤酒腐烂…”然而，如果你还没有学会它们，你可以问 Wolfram。比如试试“ [4700 欧姆电阻](https://www.wolframalpha.com/input/?i=4700+ohm+resistor)或者“[电阻红橙红](https://www.wolframalpha.com/input/?i=resistor+red+red+orange)”。

[![](img/637d653f86353fa24bc6abeedb47c38e.png)](https://hackaday.com/wp-content/uploads/2018/07/wolfohms.png)

当然，这可能会让你陷入兔子洞，问[什么是 statohm](https://www.wolframalpha.com/input/?i=statohm) ？这将导致[行为](https://en.wikipedia.org/wiki/Abohm)和其他可怕得无法想象的事情。当然，你可以随时要求“[并联电阻](https://www.wolframalpha.com/input/?i=parallel+resistors&wal=header)”，并解决等值或找到一对会给你一个理想的值。

## 技巧#4:工程单位解决方案

当然，Wolfram 主要是解方程和做微积分。例如，假设您有一个 12 伏的电池，您想要一个在空载时产生 8 伏电压的分压器。顶部电阻 R1 设置为 100ω。你可以问“ [8=12*(R_2/(R_1+R_2))，R_1=100，求解 R_2](https://www.wolframalpha.com/input/?i=8%3D12*(R_2%2F(R_1%2BR_2)),+R_1%3D100,+solve+for+R_2) ”这很管用，也是为 R1 设置像 R_1 这样的变量的简单方法。你也可以使用像 R1 这样的东西，尽管有时当你用更大的数字时会感到困惑。但是，下划线后面必须是数字。所以你可以让[成为一个更长的查询，更有象征性](https://www.wolframalpha.com/input/?i=V_2%3DV_1*(R_2%2F(R_1%2BR_2)),+R_1%3D100,+V_1%3D12,+V_2%3D8,+R_1%3D100)。

[![](img/bf64b07998a60ff31c268f441a1365c6.png)](https://hackaday.com/wp-content/uploads/2018/07/wolfdiv.png)

这很好，您可以使用并联电阻计算器计算出给定负载下的 R2 值。例如，如果负载为 333ω(约 24 mA 负载)，则 R2 的[实际值需要约为 500ω](https://www.wolframalpha.com/input/?i=parallel+resistors&assumption=%7B%22FS%22%7D+-%3E+%7B%7B%22ResistanceParallel%22,+%22R2%22%7D%7D&assumption=%7B%22F%22,+%22ResistanceParallel%22,+%22R1%22%7D+-%3E%22333%22&assumption=%7B%22F%22,+%22ResistanceParallel%22,+%22R%22%7D+-%3E%22200%22)。如果你想[仔细检查那个数学](http://tinyurl.com/y8gyv9f3)，你可以。

问题是当你得到一个小数字时，它经常以科学记数法返回。假设您不知道 Wolfram 内置了所有电抗计算器。已知电感的电抗为 2*pi*f*L，您想知道在 122 MHz 时哪个电感的电抗为 100ω。

这很容易[设置](https://www.wolframalpha.com/input/?i=100%3D2*pi*122E6*x)(我用 x 代替 L 是为了防止站点混淆单位)。你可以用 E 来表示 10 的幂，所以 122E6 就是 122 MHz。最初，它会告诉你答案是一个分数，但你可以按下“近似形式”按钮得到一个小数答案。问题是，这将显示零，直到你按下“更多的数字。”结果是 1.305 x 10 ^(-7) H。那么这是 0.13 μH 还是 130 nH？你可以让 Wolfram[帮你做](https://www.wolframalpha.com/input/?i=1.305E-7+engineering+notation)。但是，如果您要求它在一个查询中只产生工程单位的答案，这是碰运气的。

## 提示 5:它也适用于电脑

如果你对电子产品的计算机方面更感兴趣，Wolfram 也可以提供帮助。需要 [Unicode 字符](https://www.wolframalpha.com/input/?i=unicode+8800+to+8850)？需要一个 [MD5](https://www.wolframalpha.com/input/?i=MD5+%22I+read+Hackaday+every+day%22) ？也许十六进制、十进制、二进制和八进制[转换](https://www.wolframalpha.com/input/?i=354+hex+to+decimal)？你甚至可以得到关于 [IP 地址和范围](https://www.wolframalpha.com/input/?i=192.168.1.0%2F24)的信息。

我想重点是，虽然你认为 Wolfram 是数学求解器，但它知道很多事情，包括许多工程分支。也许令人沮丧的是，虽然它知道很多，但它并不知道所有的事情。因此，对于其中的每个运算放大器计算器，都少了一个分压器或所需的特定滤波器。

尽管如此，这还是节省了大量时间。如果你懂数学，你可以建立一些非常有趣的方程并求解它们。如果你不懂数学，你可以使用这个网站来看看它是如何回答某些问题的，这也很有用。