# 人工智能试图将 Python 代码转换成 C++

> 原文：<https://hackaday.com/2022/05/28/ai-attempts-converting-python-code-to-c/>

[亚历山大]创造了 [codex_py2cpp](https://github.com/alxschwrz/codex_py2cpp) 作为试验 [Codex](https://openai.com/blog/openai-codex/) 的一种方式，这是一种旨在将自然语言翻译成代码的人工智能。然而，[Alexander]的想法略有不同，他创造了`codex_py2cpp`作为一种将 Python 自动转换成 C++的方式。它并不是真的想要创建健壮的代码转换，但是就实验而言，它非常简洁。

[![](img/bcbf3f3767e4a5a91a80a7a7855e9db3.png)](https://hackaday.com/wp-content/uploads/2022/05/py2cpp-screenshot-thumbnail.png) 该程序的工作原理是读取一个 Python 脚本作为输入文件，设置一些参数，然后向 OpenAI 的 Codex API 发出转换请求。然后，它尝试编译结果。如果编译成功，那么*希望*产生的可执行文件实际上与输入文件的工作方式相同。如果不是呢？嗯，学习也很有趣。如果你试一试，也许从简单开始，不要扔太多曲球。

Codex 是一个有趣的想法，这不是我们看到的第一个以这种方式玩机器学习概念的实验。我们已经看到了[一个基于口头描述生成 Linux 命令的项目](https://hackaday.com/2021/04/20/ai-makes-linux-do-what-you-mean-not-what-you-say/)，以及[我们自己的【Maya Posch】近距离观察了 *GitHub Copilot*](https://hackaday.com/2021/08/02/github-copilot-and-the-unfulfilled-promises-of-an-artificial-intelligence-future/) ，这是一个充满承诺和概念的项目，但是——至少在当时——当它涉及到实际的实用性或有用性时，就不那么重要了。