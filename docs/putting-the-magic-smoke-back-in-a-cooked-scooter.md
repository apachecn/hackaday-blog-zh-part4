# 把魔法烟放回一辆煮熟的摩托车里

> 原文：<https://hackaday.com/2021/03/13/putting-the-magic-smoke-back-in-a-cooked-scooter/>

当[熊伟甜瓜]发现他的小米米家 M365 Pro 电动滑板车有一个定制固件(CFW)可以提高他的最高速度时，他自然就安装了它。谁不想让自己的硬件有更高的性能呢？虽然新的固件让滑板车跑得比库存更好，但对于那些可能决定比小米的好伙计们原本打算的更努力地骑他们的米家车的人来说，他确实有一个警示故事。

现在澄清一下，【熊伟】没有*而不是*因为 CFW 煮了他米家的控制板而责怪他。至少，技术上不是。新代码或其解锁的功能没有任何问题，但当与他特定的骑行风格相结合时，它只是将系统推到了边缘。失败似乎是由他在滑板车上使用最强的再生制动设置以及在下坡跑中获得的比预期高得多的速度引发的。原来显示器上闪烁的大 40 不是他的速度，而是一个指示过热情况的错误代码。哎呀。

[![](img/4f1ef573f6581935f655dae8b8661d74.png)](https://hackaday.com/wp-content/uploads/2021/03/mijiafix_detail.jpg)

Results of the PCB repair.

在带着他的滑板车尴尬的走了很长一段路回家，还被一个路人嘲笑之后，[熊伟]打开箱子，很快就发现了问题。不仅一些 MOSFETs 出现故障，PCB 上的一条迹线也被严重烧穿。从黑板上其他地方的变色来看，看起来它的几个朋友也准备加入自焚抗议。

在与他花白胡子的父亲进行了短暂的协商后，[熊伟]用更高等级的版本替换了失效的晶体管，然后将注意力转向受损的痕迹。一根电线和大量的焊料使主轨完好无损，他还对 PCB 变黑的地方进行了修补。

一个快速的测试证实了相对简单的修理就能让滑板车启动并运行，但是他如何防止它再次发生呢？在他体验过如此令人眩晕的速度后，重新安装带有更保守调节器的原始固件显然不再是一个选项，因此他需要找到一些方法来保持控制器更冷。最终的答案是使用散热垫将 MOSFETs 连接到控制器的铝制外壳上。这使得它们能够散发更多的热量，并防止类似的故障再次发生。你可能想知道为什么 MOSFETs 没有这样安装，但不幸的是，只有小米可以解释这一点。

[随着他们迅速上升的人气](https://hackaday.com/2020/06/30/the-segway-is-dead-long-live-the-segway/)黑客们已经为电动滑板车提出了[越来越多的精心改装](https://hackaday.com/2019/08/14/cheap-electric-scooter-gets-a-big-brake-upgrade-unlocks-proper-drift-mode/)，而[由于它们在二手市场](https://hackaday.com/2018/12/07/liberating-birds-for-a-cheap-electric-scooter/)的广泛可用性，当谈到这些负担得起的车辆时，最好的可能还没有到来。