# 一种抽象的钟:中国余数钟

> 原文：<https://hackaday.com/2018/08/27/an-abstract-kind-of-clock-the-chinese-remainder-clock/>

哈卡戴非常喜欢时钟。就我个人而言，在我的桌子上，我能数出至少八个钟，其中七个还在工作。有普通的石英运动模拟时钟，有趣的自动手表，普通的数字钟，一个计算器手表，以及一个非常特殊和非常坏的达斯·维德数字钟/收音机组合，很可能有一天会修好。每一个时钟都是伟大的，而人生最大的奋斗之一就是看你在死前能积累多少。时钟越独特越好，而且(到目前为止)没有什么能超过【安东尼拉·佩鲁卡】的[中国余数时钟](http://www.antonellaperucca.net/CRC.html)。

[![](img/7092261ab649e63f381e9bb7f86a8956.png)](http://www.antonellaperucca.net/CRC.html)

It’s 1:20:27 AM, the perfect writing time

将安东尼拉·佩鲁贾的钟与其他钟区分开来的是[中国剩余定理](https://en.wikipedia.org/wiki/Chinese_remainder_theorem)，这是一个来自中国数学家孙子的 1800 年前的想法。基本上，当应用于正整数时，中国剩余定理陈述了整数模某个正整数的集合`N`等价于(同构为环)整数模因子的集合`N`的乘积，使得这些因子彼此互质，并且它们的乘积是`N`。

听起来很拗口，但实际上很有直观意义。以`N = 6`为例。模 6 的整数集合是`S = {0, 1, 2, 3, 4, 5}`。2 和 3 互为互素，它们的乘积是 6。模 2 和模 3 的整数集合分别是`{0, 1}`和`{0, 1, 2}`。如果你形成这两个集合的乘积，你就得到集合`T = {(0,0), (1,0), (0,1), (1,1), (0,2), (1,2)}`。如果您从`S`中取出任意元素`x`并将其发送到`T`中的元素`(x mod 2, x mod 3)`，您很快就会看到这两组元素是如何被视为等价的。`S`中的每个元素被发送到`T`中的一个且仅一个元素，并且两个集合具有相同数量的元素。将`N`取为 6 似乎是一个容易处理的数字，但是中国剩余定理的优点表明这个相同的概念适用于任何正整数。

这如何适用于钟表呢？12 的两个相对质因数是 3 和 4。60 的三个相对质因数是 3、4 和 5。反正我们是在做时钟算术模 12 和 60。因此，我们可以直接应用我们的定理。每个小时可以用它的余数模 3 和 4 来唯一地表示。每一分钟和每一秒钟都以 3、4 和 5 为模的余数出现。在上图中，假设每个圆圈从 0 开始，每个气泡顺时针上升 1。小时是内圈，分钟是外圈，秒是分钟后面的小气泡。这时时钟开始出现。当然，你不必拘泥于那个有点熟悉的圆形钟面。你可以用数字的方式使用同样的概念，就像文章最上面的图片一样。或者你可以走得更远，完全依靠着色多边形来获得真正的抽象感。

不到一年前，Antonella Perucca 在“大学数学杂志”上介绍了这个想法，所以它还没有太多的用途。然而，用普通时钟做的任何事情都可以用这个来做，通过分享它的存在，我们有希望得到一些真正有趣的项目。看在过去的份上，它甚至可以是二进制的。