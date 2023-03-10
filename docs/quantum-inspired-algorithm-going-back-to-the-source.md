# 量子启发算法溯源

> 原文：<https://hackaday.com/2020/10/27/quantum-inspired-algorithm-going-back-to-the-source/>

最近，[Jabrils]开始完成一项艰巨的任务:[移植一种量子启发的算法，使其在(模拟的)量子计算机上运行](https://www.youtube.com/watch?v=Xe_7b9pRKY8)。算法经常受到各种自然现象的启发。例如，旅行推销员问题的解决方案[模拟蚂蚁和它们的信息素轨迹](https://hackaday.com/2020/10/21/taking-a-crack-at-the-traveling-salesman-problem/)。另一个著名的例子是神经网络，它受到你大脑中神经元的启发。然而，试图在你的神经元上运行机器学习算法，即使有笔和纸的帮助，也几乎是不可能的。

正在讨论的量子启发算法被称为[波函数坍缩函数](https://robertheaton.com/2018/12/17/wavefunction-collapse-algorithm/)。简而言之，您有一个体素立方体、一个节点图或一个平铺网格，以及一个确定节点或平铺状态的详细规则列表。在算法开始时，每个节点或点被认为处于叠加状态，这意味着它被认为处于每个可能的状态。查看规则列表，然后算法开始折叠状态。与量子计算机不同，叠加态不是经典计算机的固有部分，因此这种求解必须迭代进行。为了减少随后可能的冲突和矛盾，首先解决具有最小熵(最少数量的可能状态)的节点。首先，随机状态被分配，变化通过系统传播。这个过程一直持续到波形最终崩溃到稳定状态或达到矛盾状态。

有趣的是，规则集不需要编码，它可以从一个例子中推断出来。这种算法的一个经典用例是 2D 像素艺术级设计。通过提供小样本水平，该算法搅动并产生相似但完全独特的输出。这使得很容易从一个简单的源图像提供数以千计的独特和美丽的水平，但它是有代价的。即使是很小的水平也需要几个小时才能完全崩溃。理论上，量子计算机应该能够更快地完成这项工作，因为毕竟它是这种算法的灵感来源。

[Jabrils]花了几个星期试图让事情运行起来，但最终没有成功。然而，他的努力让我们得以一窥量子计算和这一惊人算法的世界。我们期待着从[Jabrils]那里听到更多关于这个项目的信息，他将在业余时间继续从事这项工作。也许你可以通过自学量子计算的基础知识来尝试一下。

 [https://www.youtube.com/embed/Xe_7b9pRKY8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Xe_7b9pRKY8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

