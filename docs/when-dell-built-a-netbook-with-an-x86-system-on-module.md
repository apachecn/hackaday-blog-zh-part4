# 当戴尔构建带有 X86 系统级模块的上网本时

> 原文：<https://hackaday.com/2021/12/18/when-dell-built-a-netbook-with-an-x86-system-on-module/>

就像预触摸屏手机拥有被所有人遗忘的新奇创新功能一样，笔记本电脑制造商过去也曾涉足一些领域，但现在再也不敢涉足了。在 Twitter 上，[Kiwa]讲述了戴尔[制造用户可更换 CPU+RAM 模块](https://twitter.com/kiwapebretech/status/1440080633703780355)的笔记本电脑的迷人尝试。2008 年，戴尔发布了 Inspiron Mini 1210，其 CPU、芯片组和 RAM 以“扩展的 SODIMM”外形焊接到单独的主板上，与 CM4 之前的 Raspberry Pi 计算模块没有什么不同！显然，这种“处理器卡”的不同版本存在于他们的 Inspiron Mini 系列中，具有不同数量的 RAM 和 CPU 马力。由于替换的 CPU+RAM 模块仍在网上销售，据我们所知，这使得这些戴尔上网本成为唯一具有可升级 CPU 的 x86 上网本。

如果你喜欢修补旧技术，你可以试着给自己弄一台这样的笔记本电脑或替换 CPU 模块——并且不介意在 Linux 上有次等的体验，*感谢* [波尔斯博芯片组臭名昭著的缺乏开放性](https://www.phoronix.com/scan.php?page=news_item&px=MTMyODA)。可悲的是，戴尔已经彻底放弃了 x86 模块上系统卡的概念，笔记本电脑的模块化程度越来越低-自第三代移动英特尔主板以来，我们一直没有插槽 CPU，甚至 RAM 也越来越多地焊接到主板上。理论上，“CPU 子板”方法可以提高制造产量和成本，使主板可以使用更简单的大板，而 CPU 板只能是高层数。然而，我们只能猜测，即使有所有理论上的好处，这在总体上还是不够有利可图。或者，也许是谷歌式的，有人在内部砍掉了这个项目，因为某些指标没有达到。

你想想，笔记本电脑主板是单板电脑；然而，对于我们的可升级性和可修复性的目标来说，这显然是不够的。如果你想以自己的方式升级你的笔记本电脑，而不管制造商的意图如何，这里有一个古老而令人印象深刻的故事，关于[更换最初的华硕 EEE](https://hackaday.com/2012/08/10/swapping-out-eee-pc-bga-chip-for-1-6-ghz-upgrade/) 上的焊接 CPU，以及一个最近的故事，关于[升级戴尔 XPS 超极本](https://hackaday.com/2021/11/24/you-cant-upgrade-soldered-on-laptop-ram-think-again/)中的焊接 RAM。如果你在寻找逆向计算的好处，那么[在 Twitter 上关注【基瓦】是必不可少的——最后一次看到有人扔在路边的 Kaypro 的博客修复和翻新。](https://twitter.com/kiwapebretech)