# 基于 Power PC ISA 的开放式硬件笔记本电脑

> 原文：<https://hackaday.com/2020/08/28/open-hardware-laptop-built-on-power-pc-isa/>

自从苹果在 2000 年代中期改用英特尔芯片以来，他们一直使用的摩托罗拉 PowerPC 芯片和 PowerPC 指令集架构(ISA)基本上被搁置了。虽然像超级计算这样的利基应用程序仍然在其他非苹果硬件上使用 Power ISA，但使用 PowerPC 进行个人计算的日子在很大程度上已经一去不复返了，除非你仍然拼命想让你的 Power Mac G5 不被填埋或重播《暮光之城公主》。不过，对爱好者来说幸运的是，Power ISA 现在是开源的，[这个团队一直在开发基于这种架构的开源笔记本电脑](https://www.powerpc-notebook.org/campaigns/donation-campaign-for-pcb-design-of-the-powerpc-notebook-motherboard/)。

虽然开发仍在进行中，还没有最终用户产品可用，但该小组取得的进展显示了希望。他们已经完成了他们的 PCB 设计和原理图，并有一个工作物料清单，包括一个来自 Slimbook 的机箱。也有采用 T2080RDB 开发套件和恩智浦 T2080 处理器的原型，尽管它们尚未在预期的硬件上运行。虽然仍处于初级阶段，但有一些很有前途的视频(链接如下)展示了原型在专为 Power ISA 定制的 Debian 发行版的支持下顺利运行。

我们很高兴看到这个项目的工作继续进行，因为 Power ISA 在性能上比 x86、ARM(考虑到它是非专有的)甚至 RISC-V 有许多优势，因为它更老，更好理解。如果你想对所有这些 ISA 进行更深入的比较，我们的[Maya Posch] [详细报道了这个话题](https://hackaday.com/2019/11/12/risc-v-why-the-isa-battles-arent-over-yet/)，也报道了 IBM 开源 Power ISA 的[首创之举。](https://hackaday.com/2019/08/23/joining-the-risc-v-ranks-ibms-power-isa-to-become-free/)

 [https://www.youtube.com/embed/Uf5oq0OTMu4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Uf5oq0OTMu4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

