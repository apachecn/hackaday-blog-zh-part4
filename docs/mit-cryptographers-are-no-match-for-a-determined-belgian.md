# 麻省理工学院的密码专家不是意志坚定的比利时人的对手

> 原文：<https://hackaday.com/2019/04/30/mit-cryptographers-are-no-match-for-a-determined-belgian/>

20 年前，麻省理工学院校园内一栋建筑的建造过程中包含了一个密码难题。现在的麻省理工学院计算机科学和人工智能实验室(CSAIL)所在的结构包括一个由建筑设计师[Frank Gehry]设计的时间胶囊。它包含与计算历史相关的人工制品，旨在每当有人解决了一个密码难题，或者在 35 年后被打开。

人们并不指望这个难题能早日解决，但是比利时的开发者[【Bernard fab rot】利用普通的英特尔 i7 处理器而不是超级计算机](https://www.csail.mit.edu/news/programmers-solve-mits-20-year-old-cryptographic-puzzle)成功解决了这个难题。太空舱将于五月下旬开启。

著名的密码学家罗纳德·里维斯特(Ronald Rivest)提出了一个我们现在知道的看似简单的挑战。它涉及一个连续的平方运算，并且由于它本质上是顺序的，所以不可能使用并行计算技术来走捷径。[Fabrot]在他的代码中使用了 [GNU 多精度算术库](https://gmplib.org/)，花了 3 年多的计算时间才解决。与此同时，另一个团队正在使用 FPGA，并预计在几个月内解决问题，尽管已经被比利时人击败。

最初的规范文档是一份引人入胜的读物，无论是对于谜题本身的细节，还是对于[Rivest]对计算能力未来发展方向的预测。他预计这个难题将需要整整 35 年才能解决，到 2012 年摩尔定律开始消失时，将会有 10Ghz 的处理器，但据报道，他说他低估了软件方面相应的进步。

标题图像:Tafyrn 的 Ray 和 Maria Stata 中心( [CC BY 3.0](https://en.wikipedia.org/wiki/File:MIT_Strata_Center.jpg) )