# 为更简单的 Charlieplex 进行横向思考

> 原文：<https://hackaday.com/2019/05/20/lateral-thinking-for-an-easier-charlieplex/>

在我们生活的现实世界中，PCB 往往是长方形(或者是有长方形的长方形，一直往下就是长方形)。当设计师去捕捉示意图时，东西被放在漂亮整洁的网格交叉点上；如果在布局过程中没有特别的要求，组件可能也会放在网格上。即使是最糟糕的分形轨迹网络，其路由也主要是一个层次和耐心的问题。但是，如果布局不是在 CAD 工具中完成，而是需要手工自由组装，这就不那么简单了。[【M 法则】遇到了这个问题，并发现了一个聪明的解决方案](http://crawlingrobotfortress.blogspot.com/2019/02/led-multiplexing-layouts-for-hand.html)，把事情变成对角线。

他们将适应度标准改为控制大量 led 的优化问题。驱动目标的最少引脚变成了“最简单的组装”，这意味着避免导线在布局中来回蜿蜒，这是大型 Charlieplexed 设计中的一大挫折。观察结果是，如果他们将直线 LED 矩阵旋转 45 °,并在边缘缠绕每个连接，就形成了一个本质上的大型多路复用矩阵。拓扑结构非常令人费解，所以请花一分钟时间来研究插图并构建您的心理模型。

![](img/d89b32bd6a7fa486bf9705853bc97ebe.png)

这看起来有点奇怪，但这种显示器的工作方式与普通的多路复用显示器相同，但有一个额外的好处，即每条迹线从一侧流向另一侧，而不会在任何点上打开。要点亮任何 LED，将正确的行/列对设置为源/宿，它就会打开！

如果你真的*需要*一个长方形的显示屏呢？这没问题，矩阵可以根据需要弯曲和挤压来改变它的形状。在最极端的情况下，可能的显示拓扑变得相当疯狂！下次我们需要设计一个不寻常的显示器时，我们肯定会尝试横向思考，也许会找到一个更有效的矩阵。

![](img/4b660b84084d4042ca30dd2cc10b364c.png)