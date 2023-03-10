# 机器猎豹教授马达课程

> 原文：<https://hackaday.com/2019/05/29/robotic-cheetah-teaches-a-motors-class/>

似乎现代机器人学家已经决定进行一场比赛，看看哪一组能够开发出有史以来最可怕的机器人。在撰写本文时，领先的候选人似乎是可以通过“吃”有机物来为自己提供燃料的机器人。我们只能希望相关的工程师们决定不要把那个完全具体化。无论如何，如果我们能够克服在看这些机器人时发现自己处于的可怕和/或不可思议的山谷式的情况，事实证明它们有很多东西可以教给我们许多复杂的电动马达背后的理论。

[这篇研究论文](https://dspace.mit.edu/bitstream/handle/1721.1/118671/1057343368-MIT.pdf?sequence=1)(gigant PDF warning)关注的是麻省理工学院猎豹机器人背后的建造方法。它有 12 个自由度，并使用许多成本非常低的模块化致动器作为电机来控制它的四条腿。与这种类型的其他机器人相比，这有助于他们跳过成本的主要障碍，同时仍然保持令人印象深刻的机动性和控制力。他们能够将无刷电机、带反馈的智能 [ESC 系统](https://en.wikipedia.org/wiki/Electronic_speed_control)和行星齿轮箱集成到电机本身。仅此一点就值入场费了！

他们如何做的细节在 102 页的学术文件中有详细记录，如果你需要这样的电机用于任何其他类型的项目，源代码可以在 GitHub 上找到[，但是如果你只是为了猎豹做后空翻，你也可以在该项目的博客页面](https://github.com/bgkatz/3phase_integrated)上跟上[的构建进度。我们也在](http://build-its-inprogress.blogspot.com/2019/03/hello-there-mini-cheetah.html)[的历史早期展示过这个建筑](https://hackaday.com/2014/09/15/mits-robotic-cheetah-is-getting-even-scarier/)。