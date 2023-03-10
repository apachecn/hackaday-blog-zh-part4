# 本周失败:超级电容点焊机

> 原文：<https://hackaday.com/2019/08/15/fail-of-the-week-supercapacitor-spot-welder/>

[Julian]需要将一些镍焊接到一些钢上，并决定使用点焊技术。当然，他身边没有一个点焊机。因为这些都是相当简单的机器，所以[Julian]开始用充电的超级电容器制造点焊机。基本原理似乎都在那里——超级电容是一个 100 法拉的单位，充电 2.6V，计算出超过 300 焦耳——但它就是不工作。

问题在于放电能量是如何被引导的。当你接近放电点时，仅仅使用电容器就会导致电荷以火花的形式流出。为了解决这个问题，[Julian]在电容器和铜点之间放置了一个微型开关，他希望用它作为焊接头。当然，微动开关可能不是承载大电流浪涌的最佳选择，所以我们怀疑这可能是他没有获得巨大成果的部分原因。

我们注意到的另一件事是，他使用了单点，并使用工件作为接地回路。大多数点焊机使用两个互相靠近的点或工件两侧的点。来自电容器的电流可能正好被相对较大的金属片吸收。

下面来自[美国科技]的第二个视频显示了一个 500F 的电容器用两根多一点的线进行点焊，它似乎工作正常。Hackaday 自己的[Sean Boyce]甚至用一些巨大的 3000F 帽子做了一个。这确实奏效了，尽管[他一直在追求改进](https://hackaday.com/2018/03/15/building-a-portable-solar-powered-spot-welder-nearly-practical/)。

 [https://www.youtube.com/embed/rnuWZHWshHE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rnuWZHWshHE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/cPnL0OvNMnY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cPnL0OvNMnY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

