# Linux Fu:使用校验和

> 原文：<https://hackaday.com/2022/06/22/linux-fu-roll-with-the-checksums/>

我们经常被我们花时间去优化一些东西而震惊，当我们选择一个更好的算法会更好的时候。有一个关于数学家高斯的老故事，当他在学校的时候，他被分配了从 1 到 100 的加法的忙碌工作。当其他学生费力地将每个数字相加时，高斯意识到 100+1 是 101，99 + 2 也是 101。猜猜 98 + 3 是什么？当然是 101。所以你很容易发现有 50 对加起来是 101 并且知道答案是 5050。无论你的加法速度有多快，你都不可能打败懂得这种算法的人。这里有一个问题:你有大量的文本，你想搜索它。最好的方法是什么？

当然，这是一个有内涵的问题。“最好”可能意味着很多事情，这取决于你正在处理的数据的种类，甚至取决于你正在使用的机器的类型。如果你只是在寻找一个字符串，你当然可以使用暴力算法。假设我们在《战争与和平》的文本中寻找“罪犯”这个词:

1.  从《战争与和平》的第一封信开始
2.  如果当前字母与“罪犯”的当前字母不同，则移动到下一个字母，在“罪犯”中重置当前字母，并返回到步骤 2，直到不再有字母。
3.  如果当前的字母是相同的，移动到罪犯的下一个字母，在不忘记文本的当前字母的情况下，将其与下一个字母进行比较。如果是相同的，继续重复这一步，直到“苦役犯”中不再有字母为止(此时你就有了匹配)。如果不相同，重置“罪犯”的当前字母，并返回到文本的原始当前字母，然后移动到下一个字母，返回到步骤 2。

那实际上很难用英语描述。但是，换句话说，只需将文本与搜索字符串逐字符进行比较，直到找到匹配项。这是可行的，实际上，用一些现代的硬件，你可以为此写一些快速的代码。我们能做得更好吗？

## 更好的算法

[![](img/2f3ec45b1d8b04d35e2a5b6cc96e2c73.png)](https://hackaday.com/wp-content/uploads/2022/06/search_had.jpg)

Basic search

再说一次，这真的取决于你对更好的定义。让我们假设文本包含许多几乎是我们正在寻找的字符串，但不完全是。例如，《战争与和平》中可能多次出现“the”这个词。但它也有“那里”、“然后”和“其他”，所有这些都包含我们的目标词。对于单词“the”来说，这没什么大不了的，因为它很短，但是如果您正在筛选大量的搜索字符串呢？(不知道——DNA 基因组数据什么的。)你会花很多时间去寻找死胡同。当您发现当前文本中有 199 个字符是您要查找的 200 个字符时，您会感到失望。

还有一个缺点。虽然很容易判断字符串哪里匹配，哪里不匹配，但是很难判断不匹配时是否有小的插入或删除。这对于像`diff`和`rsync`这样的工具来说很重要，他们不仅仅想知道匹配了什么，他们还想知道为什么不匹配。

事实上，正是在查看`rsync`时，我看到了`rsync`如何使用滚动校验和来比较两个文件。虽然它可能不适用于每一个应用程序，但它是您锦囊妙计中的一件有趣的东西。显然，这种“滚动校验和”算法的最佳用途之一就是`rsync`如何使用它。也就是说，它可以很快发现文件何时不同，但也可以合理地计算出它们何时恢复原样。通过滚动参考框架，`rsync`可以检测到某些内容被插入或删除，并远程做出适当的更改，从而节省网络带宽。

## 寻找

但是，您可以使用相同的策略来处理大型文本搜索。要做到这一点，你需要一个散列算法，可以很容易地放入和取出项目。例如，假设校验和算法非常简单。只需将每个字母的 ASCII 码加在一起。因此，字符串“AAAB”哈希为 65 + 65 + 65 + 66 或 261。现在假设下一个字符是一个 C，也就是“AAABC”。我们可以从第二个位置开始计算校验和，方法是减去第一个 A (65)并加上 C (67)。当然，对于这种小数据集来说很傻，但是现在你不用每次都要在数字上加几百来计算一个散列值，你只需要做一次加法和减法就可以了。

然后，我们可以计算搜索字符串的散列，并开始计算相同长度的文件的散列。如果散列码不匹配，我们知道没有匹配，我们继续前进。如果它们匹配，我们可能需要验证匹配，因为哈希通常是不精确的。两个字符串可能具有相同的哈希值。

然而，这也有一些问题。如果你只是寻找单个字符串，计算散列的成本是昂贵的。在最坏的情况下，您将不得不对每个字符进行比较、加法和减法，再加上当您遇到哈希冲突时的一些测试:具有相同哈希的两个字符串实际上并不匹配。对于正常的方案，您只需对每个字符进行测试，并对误报进行一些无用的测试。

为了优化散列算法，你可以做更好的散列。但是这也增加了计算成本，使得开销更大。然而，如果您正在寻找一串长度相同的相似字符串呢？然后你可以计算一次散列并保存它。之后的每一次搜索都会非常快，因为你不会浪费时间去调查许多死胡同，而只是原路返回。

[![](img/afb9e1052169f423be42fe071c019a9c.png)](https://hackaday.com/wp-content/uploads/2022/06/search2_had.jpg)

A hash search with a collision at ” the” when searching for “the “

我的哈希算法很简单，但不是很好。例如，您可以在示例中看到，有一个误报将导致额外的比较。当然，更好的散列算法是存在的，但是总是有冲突的可能。

使用这种哈希策略的区别有多大？嗯，我决定[写一点代码找出](https://github.com/wd5gnr/hashsearch)。我决定忽略计算搜索模式散列和滚动散列的初始部分的成本，因为这些将在足够多的交互后归零。

## 证明…有罪

如果你在古登堡计划的《战争与和平》文本中搜索“罪犯”这个词，你会发现它在 330 万个字符中只出现了四次。一次普通的搜索需要进行大约 440 万次比较才能得出结果。哈希算法以不到 430 万轻松胜出。但是哈希计算破坏了它。如果你把加和减作为两次比较的相同成本来计算，那么总共会增加大约 580 万次伪比较。

那是典型的吗？“罪犯”可能不会有太多的误报如果您运行带有单词“the”的代码，它应该有很多错误的命中，传统算法需要大约 450 万次比较，而哈希算法的调整后总数大约为 960 万次。所以你可以看到假阳性是如何影响正常算法的。

您会注意到，我的乏善可陈的哈希算法还会导致大量的误哈希阳性，这侵蚀了一些好处。一个更复杂的算法会有所帮助，但也需要一些前期计算，所以它没有你想象的那么有用。几乎任何针对任意字符串的哈希算法都会有一些冲突。当然，对于小的搜索字符串，散列可以是搜索字符串，这将是完美的，但在一般情况下这是不可行的。

代码没有保存哈希值，但是假设它保存了，并且假设第一次搜索的误报率是平均水平。这意味着，一旦预计算了哈希值，我们每次搜索可以节省 100，000 次以上的比较。所以一旦你不得不搜索 60 个左右的字符串，你就达到了收支平衡。如果您搜索 600 个字符串——但是不要忘记，它们的大小必须相同——您可以比简单的比较代码节省很多。

我实际上没有计时，因为我不想优化每一点代码。总的来说，手术越少越好。有很多方法可以提高代码的效率，如果您稍微分析一下搜索字符串，也可以应用一些启发法。但是我只是想验证我的直觉，每个算法在搜索文本上花费了多少。

## 反光

我最初是在阅读了`rsync`和备份程序`kup`的代码后开始思考这个问题的。原来这是有名字的，[拉宾-卡普算法](https://en.wikipedia.org/wiki/Rabin%E2%80%93Karp_algorithm)。有一些更好的哈希函数可以减少误报并获得额外的效率。

我的观点是什么？我并不是说 RK 搜索是你最好的方法。你真的需要一个有很多固定大小搜索的大数据集来从中获得优势。如果你考虑类似于`rsync`的东西，它实际上是使用散列来搜索两个很长的字符串可能相等的地方。但我认为在某些情况下，这些古怪的算法可能是有意义的，所以了解它们是值得的。通过写一点代码来挑战你的直觉，并得到一个算法比另一个算法好或差多少的一些估计也是很有趣的。