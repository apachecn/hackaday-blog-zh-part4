# GitHub Copilot 和人工智能未来未兑现的承诺

> 原文：<https://hackaday.com/2021/08/02/github-copilot-and-the-unfulfilled-promises-of-an-artificial-intelligence-future/>

2021 年 6 月下旬，GitHub [推出了](https://github.blog/2021-06-29-introducing-github-copilot-ai-pair-programmer/)一个他们称为 [*GitHub Copilot*](https://copilot.github.com/) 的“技术预览”，被描述为“帮助你编写更好代码的人工智能对程序员”。可以预见的是，对这一宣布的反应各不相同，从对我们的代码生成人工智能霸主的辉煌到来感到高兴，到沮丧和对厄运和黑暗的预测，因为不久公司将大批解雇软件开发人员。

像通常这种有争议的话题一样，这两个极端都与事实相去甚远。事实上，作为 GitHub 副驾驶基础的 OpenAI Codex 机器学习模型来自 OpenAI 的 GPT-3 自然语言模型，并且具有许多与 GTP-3 相同的错误和过失。所以，如果《法典》和它的《副驾驶员》并不像它被吹捧的那样好，那还有什么大不了的，为什么要展示它呢？

## 人工智能的许多定义

[![](img/230dc5075ea8a3379dd6950e2a0b26b2.png)](https://hackaday.com/wp-content/uploads/2021/07/BakerLibrary.jpg)

Baker Library at DarthMouth College. (Credit: Gavin Huang, CC BY 3.0)

建立一个真正的人工智能领域的第一次重大尝试是 1956 年的达特茅斯研讨会。这将看到数学、神经科学和计算机科学领域的一些最顶尖的头脑聚集在一起，就创造他们所谓的“人工智能”的方式进行头脑风暴，遵循当时更常见的名称，如“思维机器”和[自动机理论](https://en.wikipedia.org/wiki/Automata_theory)。

尽管在 20 世纪 50 年代和 60 年代人们抱着充满希望的态度，但人们很快认识到，人工智能是一个比最初设想的要困难得多的问题。今天，能够像人一样思考的人工智能被称为人工通用智能( [AGI](https://bdtechtalks.com/2020/05/13/what-is-artificial-general-intelligence-agi/) )，并且仍然是科幻小说的领域。我们今天所说的“人工智能”实际上是人工狭义智能( [ANI](https://bdtechtalks.com/2020/04/09/what-is-narrow-artificial-intelligence-ani/) ，或狭义人工智能)，包括接近 AGI 各个方面的技术，但这些技术的范围和应用通常非常有限。

大多数 ANIs 都基于人工神经网络( [ANNs](https://en.wikipedia.org/wiki/Artificial_neural_network) )，它们粗略地复制了生物神经网络背后的概念，例如在哺乳动物的新大脑皮层中发现的概念，尽管有很大的差异和简化。像经典神经网络和递归神经网络(RNNs)这样的神经网络——用于 GPT-3 和 Codex——在训练期间使用[反向传播](https://en.wikipedia.org/wiki/Backpropagation)进行编程，这是一个没有生物模拟的过程。

从本质上来说，GPT-3 等基于 RNN 的模型是曲线拟合模型，它使用[回归分析](https://en.wikipedia.org/wiki/Regression_analysis)来匹配给定的输入及其内部数据点，后者编码在分配给其网络内连接的权重中。这使得神经网络在其核心数学模型中，能够有效地在其参数网络中找到可能的匹配。当涉及到 GPT-3 和类似的自然语言合成系统时，它们的输出因此基于概率而不是理解。因此，与任何人工神经网络一样，这种输出的质量高度依赖于训练数据集。

## 垃圾进，垃圾出

[![](img/b60450d3b11beac411060931822ae8f9.png)](https://hackaday.com/wp-content/uploads/2021/07/Pioneer_Building_San_Francisco_2019_-1.jpg)

The historic Pioneer Building in San Francisco, home to OpenAI and Neuralink. (Credit: HaeB, CC BY-SA 4.0)

所有这些都意味着人工神经网络不具备思考和推理能力，因此不知道它生成的文本的含义。就 OpenAI 的 Codex 而言，它不知道自己写了什么代码。这导致人类检查人工神经网络工作的必然性，OpenAI 最近的一篇论文[也得出这样的结论(陈唐山等人，2021)。尽管 Codex 是在代码而不是自然语言上接受培训的，但它对工作代码的概念就像对适当的英语语法或文章写作的概念一样少。](https://arxiv.org/abs/2107.03374)

GitHub 的 Copilot 页面上的 [FAQ](https://copilot.github.com/) 也证实了这一点，它指出，在第一次尝试填充一个空白函数的代码时，它的正确率只有 43%,而在尝试 10 次后，只有 57%。陈唐山等人根据准备好的单元测试测试了从 Codex 生成的 Python 输出。他们表明，不同版本的 Codex 能够在不到一半的时间内为各种各样的输入生成正确的代码。这些输入包括从面试问题到文档字符串描述。

此外，Chen 等人指出，由于 Codex 不知道代码的含义，因此无法保证生成的代码能够运行，功能正确，并且不包含任何安全或其他缺陷。考虑到 Codex 的训练集由来自 GitHub 的千兆字节的代码组成，没有对正确性、功能或安全问题进行完全验证，这意味着回归分析得出的任何结果最多只能保证与从模糊相关的 StackOverflow 帖子中复制的代码一样正确。

## 让我们看看代码

值得注意的是，在使用 GitHub Copilot 时，OpenAI 的 Codex 是基于 [GPT-3](https://en.wikipedia.org/wiki/GPT-3) 的，它也是微软独家授权的，这也解释了它与 GitHub 的关联，以及为什么至少在当前的技术预览阶段它需要使用 Visual Studio 代码 IDE。在 VSC 安装 [GitHub Copilot 扩展](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)并登录后，你的代码会被发送到运行 Codex 的微软数据中心，供分析和建议。

Copilot 的任何代码建议都将自动提供，无需用户的明确输入。它所需要的只是一些注释，这些注释描述了应该遵循的代码的功能，并且可能还有一个函数签名。当系统发现有东西可以贡献时，它会显示这些选项，并允许用户进行选择。

不幸的是，Copilot 的技术预览版只允许非常有限的几个人访问，所以在最初的[虫族蜂拥](https://knowyourmeme.com/memes/zerg-rush)之后，我还不能获得访问权。幸运的是，一些获得访问权的人已经写下了他们的想法。

一位 TypeScript 开发者(新美乐股份公司·温尼克斯)在使用 Copilot [在 TypeScript 和 Chakra 中创建了一个最小的测验应用](https://dev.to/winnekes/i-built-an-app-with-github-copilot-here-s-the-result-2mic)后写下了他们的想法。在注释中描述了代码部分的意图后，Copilot 会建议代码，这首先包括强迫 Copilot 实际使用 Chakra UI 作为依赖。检查 Copilot 的建议通常会发现错误或不正确的代码，通过在评论中写下更明确的说明，并从 Copilot 的建议中选择想要的选项，可以修复这些代码。

新美乐股份公司的发现是，虽然 Copilot 可以与 JavaScript、Python 和 TypeScript 一起工作，并且可以在编写重复代码或单元测试时提供帮助，但生成的代码需要不断验证，并且 Copilot 经常会拒绝使用所需的模块和依赖项。生成的代码也有明显的“拼凑”感，缺乏人类开发人员所期望的一致性。最终手写这个测试花了新美乐股份公司大约 15 分钟，而迁就这个副驾驶人工智能伙伴花了两个小时。在这次经历之后，继续使用 Copilot 的热情自然降低了。

在 Scott Logic，Colin Eberhardt 和副驾驶有一段非常复杂的经历。虽然他承认有几个“哇”的时刻，副驾驶确实有点用处，甚至令人印象深刻，但负面因素最终占了上风。他的抱怨集中在打字和副驾驶弹出建议之间的延迟。这与 Copilot 使用的“自动完成”模式一起，导致了一个“工作流”,类似于一个结对编程体，它看似随机地从你手中夺走你的键盘来键入一些东西。

Colin 的经验是，当 Copilot 坚持建议 2-3 行代码时，验证 Copilot 建议的认知负荷是可以接受的。然而，当建议使用更大的代码块时，他觉得验证 Copilot 建议的开销比自己键入代码更不值得。即便如此，他也看到了 Copilot 的潜力，特别是一旦它成为真正的人工智能伙伴编程伙伴。

![Copilot might be more useful for languages that are high on boilerplate, and have limited meta-programming functionality, such as Go. --Jeremy Howard](img/0b84b6e1c02e7e00b3b44458776ab174.png)[最全面的分析](https://www.fast.ai/2021/07/19/copilot/)可能来自 Fast.ai 的杰瑞米·霍华德，他在一篇名为《GitHub Copilot 是福是祸》的博客文章中写道，Jeremy 敏锐地观察到大部分时间不是花在编写代码上，而是花在设计、调试和维护代码上。这导致了“诅咒”的部分，因为 Copilot 的(Python)代码变得相当冗长。当代码很大程度上是 Copilot 和 kin 生成的东西时，代码设计和架构(更不用说易于维护)会发生什么？

当 Jeremy 让 Copilot 生成代码来微调 PyTorch 模型时，生成的代码确实工作了，但是速度很慢，导致了不好的调整。这就引出了 Copilot 的另一个问题:对于一个给定的问题，我们如何知道给出的解决方案是最优的？当深入研究 StackOverflow 和编程论坛和博客时，您可能会发现一系列可能的方法，以及它们的优缺点。

由于 Copilot 生成的代码没有经过这样的考虑，除了通过(自动生成的)单元测试之外，生成代码的最终真正价值是什么？

## 进化，而不是革命

杰里米还指出，副驾驶并不像它自己标榜的那样具有革命性。几年来，已经有了一些选项，如 GitHub 的[语义代码搜索](https://github.blog/2018-09-18-towards-natural-language-semantic-code-search/)、[标签](https://www.tabnine.com/)和一个“人工智能助手”，可以与无数种语言(包括非脚本语言)一起工作，今年早些时候，微软发布了用于 Visual Studio 的[智能代码。这里的常见模式？基于人工智能的代码完成。](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode-insiders)

[![](img/85b84f7ed9621bc54f0001c28ecdc657.png)](https://hackaday.com/wp-content/uploads/2021/07/IntelliCodeUsageExamples.gif)

Example of Microsoft’s Visual Studio IntelliCode ‘AI-assisted development’.

鉴于 GitHub 的 Copilot 已经面临如此多的竞争，认识到它在开发过程中的位置，以及如何调整它以适应不同的开发风格变得比以往任何时候都更加重要。最重要的是，我们需要摆脱那种认为这些是“人工智能编程伙伴”的乐观想法。显然，这些更类似于雄心勃勃的自动完成算法，有它们所有的优点和缺点。

一些开发人员喜欢在 IDE 中打开所有的自动完成功能，从括号到函数和类名，这样他们几乎可以按 Enter 键来生成一半的代码，而另一些开发人员则更喜欢在充满文档和 API 引用的屏幕旁边煞费苦心地将每个字符凿入文件中。显然，Copilot 不会赢得如此不同类型的开发者。

也许反对 Copilot 和 kin 的最重要的论点是，这些只是愚蠢的算法，完全不考虑它们生成的代码。由于人类开发人员总是必须验证生成的代码，似乎 StackOverflow 等人的时代还没有结束，软件开发人员的工作仍然非常安全。