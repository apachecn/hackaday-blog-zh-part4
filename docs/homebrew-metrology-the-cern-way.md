# 欧洲粒子物理研究所的自制计量学方法

> 原文：<https://hackaday.com/2021/02/26/homebrew-metrology-the-cern-way/>

我们不会假装完全理解[这个[Marco Reps]制造的开源 8.5 位电压表](https://www.youtube.com/watch?v=D28uSzCs7-k)所发生的一切。毕竟，这个设计来自欧洲核子研究中心的奇才们，欧洲核子研究中心是欧洲核子研究的组织，是大型强子对撞机和其他大科学工具的所在地。但是我们会承认发现这个构建质量的水平绝对令人惊叹，完全值得观看视频。

正如[Marco]所说，欧洲核子研究中心即将进行的一项实验将需要大量精密电压表，其费用导致了一项自制设计，该设计在[开放硬件库](https://ohwr.org/project/opt-adc-10k-32b-1cha/wikis/home)上发布。不过，“家酿”可能有点低估了这个版本。该设计要求 ADC 具有一致的热环境，因此电路板上有一个夹层，带有精心设计的 Peltier 热控制系统，包括一个定制的散热器阻隔器。还有一个非常复杂的 PCB，专门用于在模拟输入连接器(本身就是一件机电艺术品)和机箱接地之间提供牢固的接地。

然而，这整个建筑的真正瑰宝是所使用的气相回流焊接技术。气相回流采用全氟聚醚(PFPE)溶液，沸点明确，而不是更典型的红外工艺。悬浮在加热的 PFPE 浴池上方的多氯联苯浸泡在特定温度的惰性蒸汽中。[Marco]有些简单的设置工作得几乎完美——只有一些墓碑和桥梁需要修复。对于特殊的建筑来说，这是一个很好的技巧。

我们介绍的最后一个[Marco Reps]视频是[拆除一个强大的光纤激光器](https://hackaday.com/2019/12/02/fun-with-a-200-kw-fiber-laser/)。不过，很高兴看到这样一个计量建筑，我们有一种感觉，我们会花很长时间来研究细节。

 [https://www.youtube.com/embed/D28uSzCs7-k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/D28uSzCs7-k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

