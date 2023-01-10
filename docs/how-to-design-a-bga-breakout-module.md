# 如何设计 BGA 分线模块

> 原文：<https://hackaday.com/2019/11/16/how-to-design-a-bga-breakout-module/>

对于主要习惯于使用通孔元件的黑客来说，表面贴装器件可能需要一些调整。尽管如此，最热门的新部件的诱惑甚至诱使最沉默寡言的人学习使用这项技术。当然，随着时间的推移，BGA 器件带来了更多的困难。来自 SparkFun 的[Nate]致力于开发 RedBoard Artemis，[并分解了所涉及的挑战。](https://www.sparkfun.com/news/3122)

[red board Artemis](https://www.sparkfun.com/products/15444)是一款基于 Ambiq Apollo3 芯片的 Arduino 兼容开发板。除了包装蓝牙和 1 MB 的闪存，它还能够运行 TensorFlow 模型，并使用微量的电力。该芯片采用 81 球网格阵列，间距为 0.5 毫米，这意味着 SparkFun 通常的 PCB 制造方法不会切割它。

最初运行的原型板使用 4 层、盲过孔和埋孔以及其他巧妙的技巧来分离所有必要的信号。虽然这种方法效果很好，但它既昂贵又低效。电路板上唯一需要这种加工的部分是芯片本身；板的其余部分可以用更便宜的两层方法生产。相反，为了提高这一点以便大规模生产，我们创建了一个 SMD 模块来容纳 Apollo3，然后可以根据需要将其放入更便宜的电路板上的新设计中。

[Nate]很好地解释了相关的工程，并为走类似道路的其他人分享了有用的提示。到目前为止，这只是第 1 部分，未来的帖子有望涵盖 RF 屏蔽设计和 FCC 认证过程。[【Nate】一直热衷于分享他的智慧](https://hackaday.com/2017/02/15/sparkfun-gets-back-to-their-roots-with-sparkx/)，我们迫不及待地想看看接下来会发生什么！