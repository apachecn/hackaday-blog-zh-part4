# Attiny85 上的微型机器学习

> 原文：<https://hackaday.com/2020/01/07/tiny-machine-learning-on-the-attiny85/>

我们倾向于认为机器学习(ML)的最低点在树莓派上，但它绝对不是。[EloquentArduino]一直在将极限推向规模的低端，并设法在 ATtiny85 上运行一个基本的[分类模型。](https://eloquentarduino.github.io/2019/12/machine-learning-on-attiny85/)

利用他在旧 Arduino Nano 上运行 ML 模型的经验，他已经创建了一个能够从一个`scikit-learn`导出 C 代码的[生成器](https://eloquentarduino.github.io/2019/11/how-to-create-a-classifier-for-arduino-machine-learning-projects/)。他尝试使用这个生成器为 ATtiny85 编译一个支持向量颜色分类器，但是遇到了一个问题，Arduino ATtiny85 编译器不支持生成器使用的可变函数。幸运的是，他已经试验了一种使用非变量函数的替代方法，所以他能够重新使用它并让它工作。分类器接受来自 RGB 传感器的输入，通过颜色识别一组对象。该模型最终很容易适应小型 ATtiny85 的功能，仅使用 41%的可用闪存和 4%的可用 ram。

重要的是要注意[EloquentArduino] *在这里没有做的事情:运行一个人工神经网络。就内存和计算时间而言，它们的效率太低，不适合一次安装。但是神经网络并不是唯一的游戏，如果你的任务是基于一些输入对一些东西进行分类，比如从加速度计数据中读取手势，或者从颜色传感器中命名一种颜色，这里的方法将很好地为你服务。我们想知道这是不是一个解决恼人问题的好办法，这个问题就是[通过叫声](https://hackaday.com/2019/11/21/training-bats-in-the-random-forest-with-the-confusion-matrix/)来识别蝙蝠。*

我们真的很喜欢机器学习变得如此平易近人，如果你热衷于尝试 ML，可以看看 EloquentArduino 博客的其余部分，这是一个小金矿。

我们得到了越来越多与机器学习相关的黑客，比如 Arduino Uno 上的基本[ML](https://hackaday.com/2019/06/30/blisteringly-fast-machine-learning-on-an-arduino-uno/)，以及树莓 Pi 上使用 ML 的[乐高排序](https://hackaday.com/2019/06/30/blisteringly-fast-machine-learning-on-an-arduino-uno/)。