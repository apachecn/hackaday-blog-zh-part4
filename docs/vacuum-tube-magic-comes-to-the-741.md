# 真空管魔术降临 741

> 原文：<https://hackaday.com/2021/06/19/vacuum-tube-magic-comes-to-the-741/>

你们中的一些人可能还记得最近的一个项目，一个用真空管复制的 555 定时器。它的创造者[天兔电气]在等待 555 的新 PCB 版本交付时，被留在了无所事事的地方，因此着手创建一个流行芯片的新真空管模型，[这次是无处不在的 741 运算放大器](https://www.youtube.com/watch?v=Qp4l-RWHbes)。(视频，嵌在下面。)

电路相当简单，使用六个小五极管。正如所料，前两个是长尾对，后面是两个增益级，最后一个增益级为阴极跟随器提供反馈。它整齐地构建在 PCB 上，带有由更多 PCB 材料制成的 IC 风格的“引脚”，然后放入木质基板上的 IC 插座的巨大复制体中。

结果是一个运算放大器，但不一定是一个好的。他着眼于交流性能而不是 DC，尽管这是一个完全 DC 耦合的电路，但他发现，虽然它在经典运算放大器电路中的性能与预期一致，但在较高增益下仍与理想情况有所不同。频率响应也很差，他通过用更小的值替换反馈电容来纠正这一点。遗憾的是，他没有关注它的共模性能，尽管我们预计，如果没有紧密匹配的电子管，它可能会有所欠缺。

很明显，鉴于相比之下最便宜的硅运算放大器的质量，这个项目永远不会被选为运算放大器。但它的价值在于新奇，是一个话题，也许是一个了解运算放大器的机会。为此，我们喜欢它。

[当真空管 555 的细节浮出水面的时候，我们报道了它](https://hackaday.com/2021/03/28/should-have-used-a-vacuum-tube-555/)，但是如果运算放大器是你的囊中之物[我们已经非常仔细地研究了一个简单的](https://hackaday.com/2018/02/20/deconstructing-a-simple-op-amp/)。

 [https://www.youtube.com/embed/Qp4l-RWHbes?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Qp4l-RWHbes?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[艾米丽]的提示。