# 使用 Python 在模型动物园中查找预先训练的人工智能

> 原文：<https://hackaday.com/2019/10/08/finding-pre-trained-ai-in-a-modelzoo-using-python/>

训练机器学习模型不是普通人的任务，因为这需要大量的时间或计算能力。幸运的是，人们可以使用预先训练好的模型，并且[Max Bridgland]认为编写一个 python 模块来使用命令行查找和查看这些模型是一个好主意。

对于外行人来说，Modelzoo 是一个可以找到开源深度学习代码和预训练模型的地方。[Max]接入(未记录的)API，允许用户直接查找和查看模型。当您运行一个实用程序时，它会上线并检索可用模型的类别和详细信息。从那时起，用户可以选择一个模型，应用程序将简单地打开相应的 GitHub 存储库。听起来很简单，但它有很大的价值，因为代码被设计成可扩展的，这样从事这类项目的用户也可以自动下载部分。

我们已经看到[项目使用机器学习来检测人类](https://hackaday.com/2019/01/14/project-shows-how-to-use-machine-learning-to-detect-pedestrians/)，并且使用人工智能趋势社区工具，比如这个，帮助初学者更快地入门。