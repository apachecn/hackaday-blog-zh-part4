# 卡尔曼滤波器暴露了

> 原文：<https://hackaday.com/2019/05/14/the-kalman-filter-exposed/>

如果我们雇佣一个人，比如木匠或汽车修理工，我们总是会考虑两件事:他们有什么样的工具，出问题时他们会怎么做。对于许多类型的嵌入式系统，认真的开发人员使用的一个重要工具是卡尔曼滤波器。当事情“出错”时，你也可以用它[卡尔卡诺]最近发布了一个关于[卡尔曼滤波方程](https://ngr.yt/blog/2019-04-10-kalman.html)的教程，试图揭开这个话题的神秘面纱。他举了一个例子——一个出问题的例子——当你有一个机器人，它知道它应该移动多远，也有它位置的 GPS 坐标。由于立场可能不一致，你可以认为这是系统的问题。

显而易见的答案是平均两个位置。误差小的话那还好。但是卡尔曼滤波器在更多的情况下更加稳健。[卡尔卡诺]做了很好的工作，带你通过数学，但我们会警告你，这是大量的数学。如果你不知道什么是高斯分布，或者协方差这个词让你想到帆船，你将不得不做一些阅读来阅读这篇文章。

也许我们见过的最有趣的实现是【理查德的】[交互式卡尔曼滤波模拟](https://www.cs.utexas.edu/~teammco/misc/kalman_filter/)。你可以设置所有的参数(包括随机噪声),当你移动鼠标时，网页会预测你的鼠标光标在哪里。紫色的点是嘈杂的输入，绿色的点是页面认为你的鼠标所在的位置。或者，如果你喜欢视频，有一个关于卡尔曼滤波器的 MATLAB 系列的七个视频，你可以看到下面的第一个。

这不是我们第一次看方程的[演练，但是已经有一段时间了。卡尔曼滤波器出现在令人惊讶的地方，像这个](https://hackaday.com/2012/09/10/kalman-filter-keeps-your-bot-balanced/)[相机自动对焦机制](https://hackaday.com/2014/11/12/an-external-autofocus-for-dslrs/)。

 [https://www.youtube.com/embed/mwn8xhgNpFY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mwn8xhgNpFY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

