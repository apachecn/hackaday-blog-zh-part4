# 在 X86 处理器上解锁 God 模式

> 原文：<https://hackaday.com/2019/02/03/unlocking-god-mode-on-x86-processors/>

我们错过了八月份的 Blackhat 讲座，但它太棒了，我们很高兴现在发现了它。[Christopher Domas]详细描述了他对隐藏处理器指令的痴迷，以及[他如何在某些 x86 处理器](http://www.youtube.com/watch?v=_eSAF_qT_FY)中发现一个有意的后门。这些处理器有一个辅助 RISC 内核，以及一个在该内核上运行代码的未记录的过程，绕过了正常的用户/内核分离机制。

结果是这些特定的处理器有一个故意的机制，允许任何无特权的用户直接跳转到根级别访问。演讲中最吸引人的部分是[Domas]为发现这个未记录的特性的细节所采取的系统方法。一旦他有了要寻找什么的想法，他就自动检查每个可能的 x86 指令，寻找允许在额外的内核上运行代码的指令。整个演讲既有娱乐性又有指导性，休息后来看看吧！

有大量的研究在探究复杂处理器的指令级。同样由[Domas]开发的我们最喜欢的工具之一是 [sandsifter，它可以搜索未记录的指令](https://hackaday.com/2017/07/30/find-instructions-hidden-in-your-cpu/)。

 [https://www.youtube.com/embed/_eSAF_qT_FY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_eSAF_qT_FY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

