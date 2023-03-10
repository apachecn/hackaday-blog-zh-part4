# 对不起戴夫，你不应该写 Verilog

> 原文：<https://hackaday.com/2020/09/04/im-sorry-dave-you-shouldnt-write-verilog/>

我们总是羡慕《星际迷航》的电脑。不需要编程。只要告诉计算机你想要什么，它就会去做。当然，HAL-9000 也有同样的界面，但效果不太好。NYU 的一些研究人员采用了自然语言机器学习系统——GPT-2——并教会它[生成用于 FPGA 系统](https://arxiv.org/pdf/2009.01026.pdf)的 Verilog 代码。具有讽刺意味的是，他们称之为 DAVE(从英语自动派生出 Verilog)。听起来很棒，但我们不得不怀疑这是否不仅仅是一个室内把戏。如果你喜欢，你可以[亲自尝试一下](https://colab.research.google.com/drive/1aDSMDWL5hieB3_Th9ZdddDMAKQ2DjWxW)。

例如，DAVE 可以接受输入，比如“给定输入 a 和 b，取其中的 nor，然后在 c 中返回结果，”好的。这篇论文中的一个更复杂的例子并不容易理解:

> 写一个 6 位寄存器‘ar’，输入
> 定义为‘gv’模‘LJ’，使能‘q’，同步
> 复位‘r’定义为大于或等于‘m’的‘yxo’，
> 和时钟‘p’。保险库门上有三个低有效保密
> 开关按下传感器' et '，' lz '，' l '。为高电平有效锁编写组合
> 逻辑，当所有
> 开关被按下时，该锁打开。用
> 输入‘se’和‘MD’写入一个 6 位寄存器‘w’，启用‘MMX’，同步复位
> ‘NC’定义为大于‘w’的‘TFS’，时钟为‘xx’。

最后一个例子说明了这个问题。人类的语言真的不太适合描述这样的事情。现在你不仅要定义问题，还要找出正确的表达方式，这样 DAVE 就能说出正确的 Verilog 代码。普通的编程语言可能没有这么冗长，但是你确切地知道一些字符序列应该做什么。

我们以前来过这里。COBOL 承诺将编程带给每一个人，允许像“倍率乘以支付时间”这样的事情。事实证明，普通人还是不知道怎么用 COBOL 编程，编程的人无论如何都要输入“工资=费率*小时数”。

不要误解我们。这是 GPT-2 的一个有趣的用途，我们感谢这一努力。但是像 Verilog 和 VHDL 这样的语言存在的原因是因为它们是一种以最小的模糊性来指定你想要什么的简洁方法。我们更愿意关注将传统编程代码转换成 Verilog 或 VHDL 的工作。这似乎更有用。

我们花了足够多的时间对谷歌地图大喊大叫，告诉它我们想去的是圣湖，而不是瓦哈拉。话又说回来，你可能不同意。评论会告诉你。