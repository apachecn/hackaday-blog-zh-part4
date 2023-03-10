# 联动推理软件手工去掉了硬东西

> 原文：<https://hackaday.com/2020/09/22/linkage-inferring-software-handwaves-away-the-hard-stuff/>

玩笑归玩笑，手动设计沿着特定路径移动的连杆可不是件容易的事。无论我们是在纸上涂鸦还是在 CAD 程序中限制线条，我们仍然需要做实际“想象”联动设计的工作。要是有某种工具能替我们完成所有艰难的想象工作就好了！谢天谢地，我们很幸运！这正是普渡大学的研究人员[Gen Nishida]、[Adrien Bousseau2]和[Daniel G. Aliaga1]所做的。他们设计了一个软件工具，可以让我们在特定的“关键”帧中定位重要的物体，然后软件简单地为你填充链接！

为了开始设计过程，用户输入他们的实体在最终的连接路径中需要到达的几个候选位置。从这里，这些位置被送到一个粒子过滤器。该粒子过滤器以小时间步长播种数以千计的半随机连接配置，选择一些最接近所需身体位置的最佳匹配配置，移除得分较低的结果，基于最佳匹配配置重新创建一组新的可能的关节配置，并重复进行，直到该工具收敛于尊重我们的输入关键帧的连接。

像强力搜索一样，这种解决方案需要大量的样本才能找到解决方案，但与强力搜索不同，试验会迭代地改进，使软件越来越接近最终的解决方案。在引擎盖下，软件需要实际模拟这些候选链接，以便对它们进行评分。正是在这一步，研究小组编写了额外的检查，以在重新播种之前，从这个连锁“基因库”中删除不可能的连锁，如自交关节。结果是一个为你做所有试错工作的工具——没有大脑循环。要了解更多细节，请查看他们的(开放访问！)[论文](https://www.cs.purdue.edu/homes/gnishida/mechanical/mechanical.pdf)。

增强我们机械设计能力的设计软件是这些页面上的稀有宝石，这一个也不例外。如果你想玩其他有用的联动模拟工具，试试[联动设计器](https://hackaday.com/2018/01/26/amazing-mechanical-linkages-and-the-software-to-design-them/)。如果你有心情使用其他工具来填补空白，请看看这个机器学习算法，它可以让[在视频馈送的帧](https://hackaday.com/2020/09/20/boost-your-animation-to-60-fps-using-ai/)之间填充素材。

 [https://www.youtube.com/embed/4mUKkRPaP6E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4mUKkRPaP6E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

