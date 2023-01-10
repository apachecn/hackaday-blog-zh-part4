# 帕金森勺子使用控制理论的好处

> 原文：<https://hackaday.com/2020/12/06/parkinsons-spoon-uses-control-theory-for-good/>

当我们第一次看到[Barqunics]为帕金森病患者设计的自稳定勺子时，我们想知道这样的东西能有多好。但看看下面的视频，你会发现它很好地响应了用户的手部动作，并在很大的运动范围内保持勺子完全水平。

至少有一种商业产品试图以同样的方式稳定勺子，这样遭受这种痛苦的人可以保持一定程度的独立。这表明你不需要注射成型和工厂制造的板来证明这个概念。MPU6050 提供传感器信息，两个伺服电机使用 PID 控制来控制勺子。

PID——比例、积分、微分的缩写——是一种将某些东西调整到期望点的方法。例如，考虑将一杯水加热到 95 摄氏度。如果你只是将加热器开到最大，直到达到 95 摄氏度，水实际上会变得更热，因为你会过热。使用 PID，提供的热量将取决于你现在有多远(比例)，你长期有多远(积分)，以及你最近影响了多少变化(导数)。同样的算法也适用于勺子平衡和许多其他类型的控制。

这不是我们看到的第一个[自举辅助勺子项目](https://hackaday.com/2019/01/09/adaptive-spoon-helps-those-with-parkinsons/)。不久前，我们甚至看了《T2》的商业版《T3》。

 [https://www.youtube.com/embed/LCNvCwMxjFk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LCNvCwMxjFk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

