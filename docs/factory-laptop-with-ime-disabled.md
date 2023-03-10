# 禁用 IME 的工厂笔记本电脑

> 原文：<https://hackaday.com/2020/01/28/factory-laptop-with-ime-disabled/>

不幸的是，并不是所有的消费者都高度重视他们计算机的安全性，但是有一个倾向于关注安全性的群体是拥有专门 IT 团队的企业。在为用户购买电脑时，这些群体往往有更高的要求，如确保英特尔管理引擎(IME)已被禁用。为此，Reddit 用户[netsec_burn]概述了一个非常简单的方法，让“普通人”可以为自己购买一台 IME 禁用设备。

对于那些不熟悉 IME 的人来说，它是自 2007 年左右以来所有英特尔设备上的一个协处理器，即使在计算机关机时也可以访问内存、硬盘和网络堆栈。英特尔声称这是一个功能，而不是一个缺陷，但它也是一个秘密的、未经审计的代码的来源，可以理解，这是任何试图访问计算机的恶意用户的理想目标。[netsec_burn]概述的从工厂获得禁用 IME 的计算机的方法非常简单，只需购买一台面向企业用户的特定戴尔笔记本电脑，并选择禁用 IME 的选项。

当然，戴尔警告您，如果您购买的计算机禁用了 IME，您可能会失去一些系统功能，但这似乎不会真正影响不参与系统管理的用户。还要注意，这不会*从计算机上删除*管理引擎。为此，[你将需要一台在英特尔不可能完全移除 IME 之前制造的为数不多的计算机](https://hackaday.com/2016/12/16/installing-libreboot/)。与此同时，很高兴看到至少有一家公司的计算机可以在出厂时就被禁用。