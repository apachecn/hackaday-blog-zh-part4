# 晶体管逻辑时钟堆积起来

> 原文：<https://hackaday.com/2018/09/06/transistor-logic-clock-gets-stacked-up/>

几年前，我们报道过一个非常令人印象深刻的晶体管逻辑时钟，它的布局让观察者可以看到所有的计数器在做它们的事情，并配有免费的闪光灯。它在 41 块 perfboards 上有 777 个晶体管，并且正好有零个晶体:时钟信号是从 50 赫兹的电源频率中提取的。这显然是一个爱的劳动，当然看起来令人印象深刻，但它并不是我们见过的最实用的手表。

[![](img/b22a9ffd2fdd524bd944fa7b93f367e1.png)](https://hackaday.com/wp-content/uploads/2018/09/tclock_detail.jpg) 创造者【B Brett】最近在分享新闻中写道[他的晶体管逻辑时钟第二版已经完成](https://transistorlogicclock.weebly.com/mkii.html)，我们可以自信地说这是一次胜利。他放弃了 41 个 perfboards，转而支持 9 个专业制造的 PCB，这一次是垂直堆叠的，使其对桌面更加友好。你可以拆开来研究的晶体管逻辑时钟的最终目标是一样的，但这个他称之为“MkII”的东西是这个概念的一个更精致的版本。

除了使用更少的电路板，新的 MkII 设计将逻辑电路减少到只有 283 个晶体管。这在一定程度上是由于他这次允许自己奢侈地包含了一个振荡器。该时钟使用 32.768 KHz 的标准手表晶体，其输出通过施密特触发器转换为方波。然后，将其馈入堆栈上方的分频器，该分频器使用触发器产生 1Hz 和 2Hz 信号，供时钟的其余部分使用。

除了这个项目的[原版，我们还看到了一个](https://hackaday.com/2016/06/01/transistor-logic-clock-has-777-transistors/)[漂亮的单板壁挂版](https://hackaday.com/2010/01/11/194-transistor-clock-will-blow-your-mind/)，甚至还有一个[“死虫”风格的用边角料搭建的](https://hackaday.com/2015/05/04/building-a-transistor-clock-from-scrap/)。

 [https://www.youtube.com/embed/KQEDJgZ_4Q8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KQEDJgZ_4Q8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

