# 你认为你知道马里奥赛车是怎么工作的吗？

> 原文：<https://hackaday.com/2022/07/04/think-you-know-how-mario-kart-works/>

在看起来像一个有趣的视频系列的开始中，[MrL314]带我们快速而深入地参观了《马里奥赛车》中的人工智能如何工作。(视频，嵌在下面。)不怎么玩马里奥赛车了？好吧，无论如何都要看一看，因为让布瑟与桃子公主擦肩而过而不撞上她的一些非常简单的技巧可能在任何预先编程的导航场景中都有用。

快速剧透。CPU 玩家穿过不同的区域，每个区域都有一个期望的速度和一个向量方向场，可以改变他们应该指向的方向。只有当它们偏离航向时，它们才会计算出目标的航向。预先设置这个期望的方向和速度大大减少了所需的实时计算。

然后你把其他选手也加入进来，一个非常简单的距离相关转弯算法就能实现干净利落的超车。不过，这种效果是为特定的赛道手工调整的，因为你不想让 Luigi 在彩虹路上开出狭窄的路段。更多技术细节可以查看【MrL314】的笔记。

如果说有什么不同的话，这个视频让我们对那些聪明的小技巧有了进一步的认识，这些小技巧从极其简单的规则中创造出看似复杂的交互。当你在下一个几千兆字节的神经网络模型中编程时，记住马里奥赛车，好吗？

 [https://www.youtube.com/embed/oq4Wu1PjukI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oq4Wu1PjukI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

