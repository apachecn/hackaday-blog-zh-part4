# 随机马尔可夫节拍

> 原文：<https://hackaday.com/2021/02/20/stochastic-markov-beats/>

[Attoparsec]在他的 YouTube 频道上建立有趣的音乐项目已经有一段时间了，他的最新作品也不例外。简称为“节点模块”，它是一个基于硬件的[机架式马尔可夫链节拍序列发生器](https://www.youtube.com/watch?v=gvnHzsNJ92k)。传统上，[马尔可夫链](https://en.wikipedia.org/wiki/Markov_chain)是软件状态机，以给定的概率在状态之间转换，通常从训练语料库中学习。同样的原理也适用于硬件节拍排序。

每个节点模块都有一个触发输入、四个输出(每个输出都有一个电位计)和一个触发输出。[Attoparsec]在视频开始时对组成该模块的所有不同部分和理论进行了精彩的解释，但基本操作是输入一个触发信号，读取电位计以确定每个输出的概率。一个被随机选中并被解雇。正如您所想象的，存在循环甚至死端节点，对于一些音乐作品，预期有一定数量的节拍，因此可以发送一个聪明的重置信号，以定期将链拉回到初始的开始状态。结果听起来很有趣，想象所有的可能性更好。

该模块本身是一个基于 Arduino 的定制 PCB，布局非常简洁。如果你想自己做一个，BOM、代码和 KiCad 文件[都可以在 GitHub](https://github.com/attoparsec/Node) 上找到。这不是[制造的第一台仪器，我们相信这不会是最后一台。](https://hackaday.com/2011/10/21/hydrocrystallophone-probably-wont-make-you-insane/)

 [https://www.youtube.com/embed/gvnHzsNJ92k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gvnHzsNJ92k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[smellsofbikes]发送此邮件！