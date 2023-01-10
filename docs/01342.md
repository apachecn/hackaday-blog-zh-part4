# 值得一试的神经网络馅饼

> 原文：<https://hackaday.com/2018/11/22/neural-network-pies-that-might-be-worth-a-try/>

神经网络是机器学习领域的一项关键技术。一种常见的技术是用样本数据训练他们，然后要求他们以同样的方式创造新的东西。人工智能研究人员[Janelle Shane]决定给神经网络一个有趣的任务——发明新的馅饼。

使用 [char-rnn](https://github.com/karpathy/char-rnn) 库，网络最初在来自互联网的 2237 个馅饼食谱标题样本上被训练。早期的迭代甚至很难拼出“pie”，但是随着网络的改进，结果也是如此。我们甚至无法想象如何做一个“瑞典馅饼”，相比之下，后来的结果，如“不可能的枫叶菠菜苹果派”似乎更复杂。

在这一点上，[Janelle]决定混合一些东西，[加入另一个由各种饼干和苹果的名字组成的样本](http://aiweirdness.com/post/180349337437/how-to-make-high-tech-pies-sound-really-old)。这些数据被仔细分类，因此网络仍然优先考虑 pie，但是这些额外的数据给了模型一个更丰富的库。这导致了家庭烘焙的经典，如 Flangerson 的大红挞和鸡肉菠萝奶油馅饼。

从表面上看，这是一个有趣的项目，有着异想天开的产出，但从根本上来说，它凸显了如今站在巨人的肩膀上可以完成多少工作。我们以前也看到过[Janelle]的输出——[命名西红柿。](https://hackaday.com/2018/04/26/neural-network-names-nightshades/)