# 存在感探测垫让你不会坐以待毙

> 原文：<https://hackaday.com/2022/08/11/presence-detecting-cushion-keeps-you-from-sitting-your-life-away/>

他们说坐着是新的吸烟方式。他们错了——对你来说，吸烟比坐着更糟糕，只有站着或绕着街区慢跑时才吸烟，这并不能证明这个习惯是正确的。但是他们也没有说错，人类并不是生来就长时间靠着屁股的，但是我们还是这样做了，这损害了我们的心脏健康、姿势和总体健康。所以像[这种检测臀部的站立提醒](https://hackaday.io/project/186775-prolonged-sitting-alarm)会对你的健康产生很大的影响。

虽然像我们许多人一样，[戴夫·贝内特]有一个可穿戴设备，在检测到坐着 30 分钟后，它会提示他起身走动，但他发现，忽视警报并继续坐着太容易了。他觉得自己需要更多一点的鼓励才能起身离开，于是他完全从零开始建造了一个存在探测器。他的传感器是一片包裹在导电胶带中的静电防护 Velostat 泡沫；压缩时，焊盘上的电阻下降，因此很容易用简单的比较电路进行检测。

我们承认，当我们第一次看到报警电路时，我们很兴奋；快速浏览一下原理图，似乎是基于 555，这完全有可能。但是没有，[Dave]的设计目标包括防止通过快速“偷偷摸摸”欺骗警报，这在代码中最容易实现。因此，电路中的 8 引脚器件是 ATtiny85，它会在 30 分钟后发出警报，并要求他在复位前保持一分钟不动。下面的视频触及了设计的高点，并展示了它的使用。

烦人？是的，但这才是重点。当然，立式办公桌也会起到同样的作用，但这并不适用于所有人，所以这是一个不错的选择。

 [https://www.youtube.com/embed/lPFiY0v1rcI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lPFiY0v1rcI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

