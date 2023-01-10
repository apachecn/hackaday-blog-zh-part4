# 人工智能准备把互联网变成胡言乱语

> 原文：<https://hackaday.com/2019/08/31/ai-poised-to-turn-the-internet-into-gibberish/>

上周四，两个卑微的硕士研究生 Aaron Gokaslan 和 Vanya Cohen 设法复制了秘密的 OpenAI 模型，并厚颜无耻地将他们的版本命名为 OpenGPT-2。代码可以从这个 [Google Colab 页面](https://colab.research.google.com/drive/1esbpDOorf7DQJV8GXWON24c-EQrSKOit#forceEdit=true&offline=true&sandboxMode=true)下载，显然使用它不需要语言建模方面的经验。更有用的可能是说服谷歌放弃价值 5 万美元的免费云计算培训时间所需的技能！

研究公司 [OpenAI](https://openai.com/) 发布了一个新的、更强大的 GPT 语言模型版本，拥有 15 亿个参数，在 800 万个网页的数据集上进行训练，尽管它最有趣的用途是产生胡言乱语，但它不可避免地也会很快产生连贯的文本。对于我们这些凡人来说，有一个运行在云中的简化版模型和一个我们可以访问的[网页](https://talktotransformer.com/)，输入一个简短的短语来提示系统，并打印出几段假新闻。我们尝试了以下内容:“您可以使用 Arduino 来”,结果是:

*   你可以用 Arduino 来切除阑尾。使用开环或闭环，但不要同时使用，即不要像我一样将 Arduino 连接到墙上。Arduino 的噪音很大，会损坏电路板。一定要用质量好，质量高的电阻把它们接到墙上。如果你愿意，你也可以使用自己的天线。

神经网络的工作原理是获取之前打印的文本，并使用它来预测下一个单词。由于它的晦涩难懂，我们的 Arduino 示例是对处于羽翼未丰的婴儿状态的系统的一个相当严重和相当不公平的测试，并且，从适当的指标来看，它实际上在某些标准行业测试集上表现得相当好，例如[儿童书籍测试](https://uclmr.github.io/ai4exams/data.html)。

请务必将您自己的假新闻粘贴到下面的评论中，我们将投票选出最有趣的一条，但请保持在良好品味的范围内！

虽然这是一项新兴技术，但不久前确实有人得到了它，并将其应用到一台旧的电传打字机上！