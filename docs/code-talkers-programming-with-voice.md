# 代码说话者:用语音编程

> 原文：<https://hackaday.com/2021/03/28/code-talkers-programming-with-voice/>

IEEE Spectrum 有一个有趣的帖子，报道了几家试图出售语音编程接口的公司。不是为语音识别编程 API，而是代替传统的文本编辑器来制作程序。

Serenade 和 Talon 这两家公司风格迥异。小夜曲的语言听起来相当正常，而 Talon 让你使用非常具体的短语，甚至可以使用眼球追踪来判断你发出命令时在看什么。还提到了两个开源产品(Aenae 和 Caster ),它们需要你使用第三方语音引擎。

作为 Talon 输入的一个例子，假设您希望在您的程序中包含这行代码:

```
name=extract_word(m)
```

你会大声说:“短语名称 op 等于 snake extract 单词 paren mad。”这与《星际迷航》设想的语音编程并不完全一样。

对于可访问性，这可能是可行的。我们很难想象一屋子的开发人员都在谈论如何让他们的计算机输入 C 或 Python 代码。直到我们可以说，“计算机，使用文件 hackaday-27 中的数据建立一个图形，”我们认为这不会成为主流。

实际的[语音识别部分](https://hackaday.com/2019/01/01/picovoice-puts-smarts-offline-in-512k-of-memory/)现在几乎是一种商品。对人们会说什么以及他们的意思做出合理的猜测是另一回事。当你有非常具体和有限的词汇时，这似乎最有效，比如操作[一台 3D 打印机](https://hackaday.com/2018/01/05/teaching-alexa-to-3d-print/)。