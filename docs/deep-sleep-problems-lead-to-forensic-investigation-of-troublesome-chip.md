# 深度睡眠问题导致对有问题芯片的法医调查

> 原文：<https://hackaday.com/2020/09/15/deep-sleep-problems-lead-to-forensic-investigation-of-troublesome-chip/>

当你购买一个芯片时，你如何确定你得到了你所支付的？毕竟，它只是一个黑色的塑料斑点，上面有一些导线伸出来，还有一些激光蚀刻的标记证明了里面的东西。当然，所有这些都很容易伪造，一旦你在电路中试用，就很容易判断你是否有缺陷的芯片。

但是品牌外的芯片呢？这些芯片可能功能相似，但在某些关键方面仍然不合规格。Kevin Darrah 就是这样，这导致了他对可能假冒的 MCU 芯片的法医分析。[Kevin]注意到他的一个 ATMega328 项目在深度睡眠模式下消耗了太多的能量——大约多了两个数量级。下面的第一个视频显示了他对问题的初步调查和描述，包括从有问题的芯片所在的开发板上移除该芯片，并将其放在一个分线板上，该分线板在深度睡眠中的功耗应小于 1 微安。显示它提取了 100 μA 反而敲定了交易——芯片出了问题。

[Kevin]然后将可能是伪造的芯片送到实验室进行全面的法医分析，因为当然有公司以此为生。下面的第二个视频显示了外部检查，没有发现任何结论性的东西，随后是 X 射线分析。这揭示了足够的怪异之处，足以证明破坏性测试是正确的，这表明了一个令人遗憾的事实——可疑单元中的芯片与 Atmel 芯片的芯片完全不同。

很难说这个芯片是假货；毕竟，Atmel 可能与另一家代工厂签订了某种合同来生产 MCU。但在购买廉价芯片时，这显然是一个需要记住的问题，尤其是那些功能测试几乎符合规格的芯片。顾客小心上当。

假冒零件非常普遍，这是我们以前多次提到的话题。如果你想了解更多，先从指南开始。

 [https://www.youtube.com/embed/PlGycKwnsSw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PlGycKwnsSw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/o0rEzcKYzGw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/o0rEzcKYzGw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提醒。