# 训练神经网络来玩驾驶游戏

> 原文：<https://hackaday.com/2020/11/07/training-a-neural-network-to-play-a-driving-game/>

通常，当我们想到让计算机完成一项任务时，我们会考虑创建复杂的算法，接受相关的输入并产生所需的行为。对于某些任务，比如在路上驾驶汽车，大量的输入数据及其与期望输出的关系非常复杂，以至于几乎不可能编写解决方案。在这些情况下，创建一个神经网络并训练计算机来完成这项工作可能更有意义，就像人类一样。在更基本的层面上，[Gigante]就是这么做的，[用遗传算法教神经网络玩基本的驾驶游戏。](https://www.youtube.com/watch?v=wL7tSgUpy8w)

该游戏由一个基本的自上而下的 2D 驾驶游戏组成。AI 给出了从车辆前方以不同角度投射的五条线到轨道边缘的距离。人工智能也知道它的速度和方向。给定这 7 个数字，它计算出驾驶汽车的转向、制动和加速输出。

为了训练人工智能，[Gigante]从 650 个人工智能开始，并挑选了表现最好的人工智能，这些人工智能只能勉强通过前两个弯道。将这种人工智能标记为下一代的父母，人工智能以随机突变进行迭代。每一代都有所进步，Gigante 每次都会挑选表现最好的来养育下一代。在仅仅四次迭代中，一些赛车能够完成一整圈。经过足够的训练，这些汽车能够以极快的速度完成全程，而不会撞到墙上。

这是机器学习和使用遗传算法来随着时间的推移提高适应性的一个很好的例子。[Gigante]指出，如果软件被编码成可以自我测量每一代人的适应度，那么也不需要人参与进来。我们也见过类似的技术用于玩马里奥。休息后的视频。

 [https://www.youtube.com/embed/wL7tSgUpy8w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wL7tSgUpy8w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

