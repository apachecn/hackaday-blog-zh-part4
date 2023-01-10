# 将 SNES Rom 修改为宽屏

> 原文：<https://hackaday.com/2021/06/22/modifying-a-snes-rom-to-be-widescreen/>

将像《SNES 超级马里奥世界》这样的游戏转变成一款宽屏游戏并不是一项小任务，但是[熊伟·比莱拉]做到了。[熊伟]有一长串令人难以置信的补丁，如优化代码以获得更好的帧速率，并添加代码以利用 [SA-1 加速器芯片](https://sneslab.net/wiki/SA-1)，因此他比任何人都知道如何实现宽屏模式。这个补丁代表了真正的爱的劳动，因为许多关卡都是按照特定的屏幕宽度设计的。[熊伟]经历了每一个单屏幕宽度级别，并通过编写所需的额外程序集来扩展它们。

在技术层面上，这种攻击是通过使用游戏内置的平移功能实现的。左肩和右肩按钮允许玩家向左和向右移动摄像机。视口被认为是屏幕分辨率的两倍，因此项目将在宽屏分辨率内呈现。通过取消平移功能并将更大的视口部分渲染到屏幕上，您可以获得宽屏视图。然而，为了节省周期，敌人和物品直到接近屏幕边缘才开始移动。那么，如何在不破坏每一个产生的敌人的时间的情况下制作游戏宽屏呢？突然间，粉丝们多年来训练的肌肉记忆时间成了一种劣势，而非优势。答案是大量的时间投入和对细节的关注。

所有代码都可以在 GitHub 上找到。休息之后是一段关于国防部的视频。

 [https://www.youtube.com/embed/KrMhpJl-BQk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KrMhpJl-BQk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

