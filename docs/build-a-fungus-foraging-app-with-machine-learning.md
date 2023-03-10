# 用机器学习构建真菌觅食 App

> 原文：<https://hackaday.com/2019/08/22/build-a-fungus-foraging-app-with-machine-learning/>

随着 2019 年蘑菇觅食季节的临近，是时候将我对低级机器学习(ML)的求知欲与我居住的地方的一种流行消遣结合起来了。声明一下，我不是 ML 方面的专家，我只是邀请读者跟随我回到我最近探索的一些兔子洞。

![](img/d1f7a9557fec5377be5a6ab31246bc3e.png)但是蘑菇，我知道一点，所以首先，关于健康和安全:

*   创建的应用程序应该非常谨慎地使用，并且结果必须得到真菌专家的确认。
*   总是测试真菌，开始只吃很小的一片，等待几个小时，以检查有没有不良影响。
*   一定要戴手套——手指很容易吸收毒素。

因为这是对 ML 的介绍，所以不会有太多的术语，重点将放在享受乐趣上，而不是进行深入探讨。我偶然发现的系统叫做 [XGBoost](https://github.com/dmlc/xgboost) (XGB)。XGB 演示之一是二进制分类，而[数据](https://github.com/paddygoat/xgboost/blob/master/demo/binary_classification/agaricus-lepiota.data)取自[奥杜邦协会北美蘑菇野外指南](https://www.amazon.com/National-Audubon-Society-American-Mushrooms/dp/0394519922)。二进制意味着应用程序给出“是”或“否”的概率，在这种情况下，它倾向于给出大约 95%的概率，即一个普通的食用菌( [蘑菇](https://en.wikipedia.org/wiki/Agaricus_campestris) )实际上是可食用的。![](img/8e2e683e0696a1f0fdb146a429282823.png)

该应用程序向用户询问了 22 个关于他们样本的问题，并将输入的数据整理成一系列用逗号分隔的字母。在调查问卷结束时，该数据行被写入一个名为“fungusFile.data”的文件，以供进一步处理。

XGB 不能接受字母作为数据，所以必须将它们映射为“经典 LibSVM 格式”，每个字母如下所示:“3:218”。接下来，这个 XGB 友好数据被分成两部分，用于训练模型，然后测试该模型。

[与更高级别的深度学习系统相比，安装 XGB](https://github.com/paddygoat/xgboost/blob/master/demo/binary_classification/README.md) 相对容易，并且在 Linux Ubuntu 16.04 和 Raspberry Pi 上都运行良好。我在`bash`中写了[部署应用](https://github.com/paddygoat/xgboost/blob/master/demo/binary_classification/questions_01.sh)，所以不应该有任何额外的软件需要安装。在更深入地了解 ML 之前，我强烈建议安装 XGB，运行这个应用程序，并尝试一下。

通过在终端运行`bash runexp.sh`进行训练和测试，处理 8124 行真菌数据不到一秒钟。最后，bash 给出了一组统计数据来表示训练的准确性，并试图“画出”XGB 设计的决策树。如果我们快速查看一下目录`~/xgboost/demo/binary_classification`，现在应该有一个`0002.model`文件准备好与问卷一起部署。

我有兴趣进一步探索决策树，看看 XGB 对真菌的不同特征进行加权的方式。我最终在一个基于 Python 的 [Jupyter 笔记本脚本上得到一些粗略的可视化效果:](https://github.com/paddygoat/xgboost/blob/master/demo/binary_classification/Mushrooms_02.ipynb)

![](img/46b9d501f96e23d744fb23dd93395906.png) ![](img/5b9072f75ab4323907b978e0c6658599.png)

显然，这个应用程序不会赢得任何 Kaggle 比赛，因为软件中的各种参数需要在所有不同软件工具的帮助下仔细调整。一个好的开始是调整树的最大深度和使用的树的数量。深度= 4 和数量= 4 似乎适用于此数据。其他参数包括特征重要性类型，例如:增益、权重、覆盖、总增益或总覆盖。这些可以使用工具来调整，如 [SHAP](https://github.com/paddygoat/shap) 。

最后，这个应用程序可以很容易地适应其他基于问卷的系统，如诊断特定的疾病，或决定是否购买特定的股票或市场份额。

[更基本的 ML 介绍](https://hackaday.com/2016/11/02/machine-learning-foundations/)更详细地介绍了基线理论——很值得快速浏览一下。