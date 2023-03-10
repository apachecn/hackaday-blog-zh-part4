# 路德维希承诺向优步学习简单的机器

> 原文：<https://hackaday.com/2019/02/25/ludwig-promises-easy-machine-learning-from-uber/>

机器学习带来了一个古老的想法——神经网络——来解决一系列以前难以解决的问题，如手写和语音识别。更好的软件和硬件使得应用复杂的机器学习算法变得可行，这在以前只能在巨型超级计算机上实现。然而，开发模型和软件来使用这些经过训练的模型仍然需要一个学习过程。优步——你知道，当你有点喝多了的时候开车送你回家的那些人——有他们所谓的“无代码深度学习工具箱”,名为 [Ludwig](https://eng.uber.com/introducing-ludwig/) 。承诺是您可以创建、训练和使用模型来从数据中提取特征，而无需编写任何代码。你可以在 GitHub.io 上找到[这个项目本身。](https://uber.github.io/ludwig/)

工具箱建立在 TensorFlow 之上，他们声称:

> Ludwig 的独特之处在于，它能够帮助非专家更容易理解深度学习，并为经验丰富的机器学习开发人员和研究人员等提供更快的模型改进迭代周期。通过使用 Ludwig，专家和研究人员可以简化原型制作过程，并简化数据处理，以便他们可以专注于开发深度学习架构，而不是数据争论。

Ludwig 的关键在于它附带了许多模型架构。您可以添加自己的模型，但是在许多情况下，使用内置的模型将允许您快速启动并运行模型。您不必编码，但您必须构建一个 YAML 配置文件，这并不坏。有许多已知的数据类型，如文本和图像，这也有助于简化配置。

帖子展示了一个简单的例子。包含书籍的类似电子表格的数据库是训练数据。它包含书名、作者、描述、封面图片、流派和价格。我们的目标是学习这个数据集，然后针对未来的数据，预测类型和价格。YAML 文件非常简单:

```
input_features:
 –
   name: title
   type: text
 –
   name: author
   type: category
 –
   name: description
   type: text
 –
   name: cover
   type: image
output_features:
 –
   name: genre
   type: category
 –
   name: price
   type: numerical
training:
 epochs: 10
```

如果你想选择选项，你可以把它变得更复杂。例如，默认情况下，文本字段使用 CNN 编码器，但是您可以覆盖它并选择 RNN。

Ludwig 本身就是一个命令行程序，采用命令行。当然，训练命令会生成一个模型。visualize 命令生成损失和准确性的图表。predict 命令将新数据应用于模型。你可以在他们的网站上看到许多其他的[例子。如果你决定真的要写代码，Ludwig 公开了一个 Python 接口。](https://uber.github.io/ludwig/examples/)

如果你决定更进一步，你可以在你的浏览器中运行 [TensorFlow。你甚至可以阅读](https://hackaday.com/2018/04/16/tensorflow-in-your-browser/)[我们自己的教程](https://hackaday.com/2017/04/11/introduction-to-tensorflow/)。