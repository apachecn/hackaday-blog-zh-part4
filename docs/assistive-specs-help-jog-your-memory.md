# 辅助眼镜有助于唤起你的记忆

> 原文：<https://hackaday.com/2020/03/01/assistive-specs-help-jog-your-memory/>

我们每个人都可能会忘记一些事情。无论老少，我们都知道事情在我们的待办清单上，但在最激动的时刻，它们从我们的脑海中消失了，我们想念它们。有无数的技术方法可以解决这个问题，比如提醒和日历，但是尼克·比尔德提出了可能是迄今为止最有创意的方法。他的 Newrons 项目是一副带有机器视觉摄像头的眼镜，当它检测到视野中与日历条目相关的物体时，就会发出闪光。

它的核心是 JeVois A33 智能机器视觉相机，它运行在图像数据集上训练的神经网络。它将自己的发现传递给一个装有实时时钟的 Arduino Nano 物联网，该物联网从谷歌日历中提取约会信息，并在检测到对象和事件匹配时闪烁 LED。我们放在休息时间下面的例子是一个药瓶，它触发服药提醒。

我们喜欢这个想法，但不禁认为它有一个缺陷，即提醒依赖于物体进入视野。一个将这一点与基于日历的更传统的提醒结合起来的版本将解决这一问题，并可能为健忘的人节省一些问题。

 [https://www.youtube.com/embed/C8D3Lubc3Jo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/C8D3Lubc3Jo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

