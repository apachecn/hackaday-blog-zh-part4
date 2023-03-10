# 如何识别假运算放大器

> 原文：<https://hackaday.com/2022/02/05/how-to-spot-a-fake-op-amp/>

我们都知道，如果你准备在正确的地方寻找，就会发现大量的假组件，拍卖网站上可能好得难以置信的芯片报价可能会有一些标记，这些标记会擦掉，露出下面完全不同的东西。[IMSAI Guy]看到一批 OP-07 激光调整运算放大器，价格很便宜，[于是拿起它们进行调查](https://www.youtube.com/watch?v=cOC9aj_jtwo)。可以看看休息下面的视频。

当两个输入电压相同时，完美的运算放大器具有零伏输出，但实际上没有真正的器件能达到这种完美水平。它被称为失调电压，对于低失调电压至关重要的仪器仪表工作，OP-07 等器件均已通过激光进行调整，将其元件调整至最低失调。这种工艺很贵，所以正版 OP-07 自然也贵。

在这种情况下，识别真假运算放大器非常简单，只需将芯片连接成单位增益同相放大器，然后测量输出端的电压(我们不禁对 Keithley 2015 THD 万用表产生一丝羡慕！)，根据该测量，假货应该是清晰可见的。首先是一些失调电压大于 1 mV 的 741(尽管异常值 741 的失调电压为 40μV ),以展示廉价运算放大器的预期性能，然后我们来看看 OP-07。当偏移超过 1.2 mV 时，我们可以立即断定它们是假的，正如他所承认的那样，这个价格并不令人惊讶。与此同时，我们将密切关注韩国制造的 741，如异常低偏移设备。

如果你对运算放大器内部感兴趣，我们可以建议[看看第一个 IC 运算放大器](https://hackaday.com/2018/02/20/deconstructing-a-simple-op-amp/)，同时[这不是我们看到的第一个假芯片](https://hackaday.com/2017/08/22/fake-ram-identifying-a-counterfeit-chip/)。

 [https://www.youtube.com/embed/cOC9aj_jtwo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cOC9aj_jtwo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢鲍尔的提示。