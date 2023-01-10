# 差异工具知道你的意思

> 原文：<https://hackaday.com/2022/09/10/diff-tool-knows-what-you-mean/>

我们承认自己并不特别艺术，但我们确实记得一位美术老师告诉我们，有时画不存在的东西比画存在的东西更好——这是一个被称为负空间的概念。[Wilfred]在解释他的“奇妙差异”工具时提出了类似的观点，该工具被恰当地称为 [difftastic](https://www.wilfred.me.uk/blog/2022/09/06/difftastic-the-fantastic-diff/) 。他指出，当比较两个程序时，目标不是确定什么发生了变化，而是什么保持不变。你越能认同相同，你就越不需要表现出变化。

该工具以一种智能的方式比较源代码，借助于已经解析了许多不同语言的 [tree-sitter](https://tree-sitter.github.io/tree-sitter/) ，至少对于这个目的来说已经足够好了。根据[Wilfred 的]帖子，该工具支持 44 种不同的语言，从 bash 和 YAML，从 Verilog 到 VHDL，从 C++到 Rust，等等。

当然，这个工具本身是值得注意的。但是文章中真正的精华是像 tree-sitter 和算法的清晰描述(借用自 [autochrome](https://fazzone.github.io/autochrome.html) )这样的东西，用于计算最小的变化集。

代码仍在开发中，输出并不总是像他希望的那样清晰。尽管如此，这仍然是一个非常好的工具，也是一篇关于开发挑战的精彩文章。

虽然 Verilog 和 VHDL 是一个开始，但我们真的希望 diff 用于[原理图](https://hackaday.com/2018/09/19/visual-schematic-diffs-in-kicad-help-find-changes/)。哦，还有 [PCB 布局](https://hackaday.com/2011/10/14/hardware-version-control-using-visual-diff/)，也别忘了那些。