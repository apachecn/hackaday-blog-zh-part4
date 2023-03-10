# 32 位真的死了吗？

> 原文：<https://hackaday.com/2021/06/06/is-32-bits-really-dead/>

当我们中的一些人仍然坚持使用我们最喜欢的 8 位微处理器时，ARM 宣布他们将在 2022 年和/或 2023 年淘汰 32 位架构。在 GaryExplains YouTube 频道上，[Gary Sims] [发布了一篇关于当前 32 位与 64 位事态的精彩评论](https://www.youtube.com/watch?v=jlRAnO1GR0U)——不仅针对 ARM，也针对英特尔和 AMD 处理器。对你们这些 32 位粉丝来说，这是一个令人沮丧的前景。

ARM [去年秋天](https://www.anandtech.com/show/16584/arm-announces-armv9-architecture)宣布，到 2022 年将不再有 32 位支持，然后[今年 3 月他们也发布了类似的公告](https://www.arm.com/blogs/blueprint/64-bit)，但最后期限是 2023 年。[Gary]试图解析这些陈述，并对差异意味着什么进行有根据的猜测(剧透警告——他预测不久将发布另一个 32 位内核)。

[Gary]显然，Linux、Windows、MacOS、Android 和 iOS 等操作系统打破了 32 位的局面，以及近年来所有这些操作系统如何过渡到 64 位。他做了一个彻底的工作，并得出结论，过渡已经顺利进行。虽然 Linux 和 Windows 还没有完全放弃 32 位支持，但这已经是板上钉钉了。

然而，请注意，本文讨论的是 Cortex——智能手机、平板电脑、电脑和强大的嵌入式应用(如自动驾驶汽车)中的一系列内核。流行的 32 位 Cortex-M 系列低成本/低功耗内核用于许多嵌入式系统设计，在可预见的未来仍将是 32 位内核。

在观看了[Gary]的演示之后，如果您想了解更多信息，[请查看几周前[Maya Posch]就最新 ARMv9 ISA 的细节所做的文章](https://hackaday.com/2021/05/10/the-armv9-isa-and-what-it-can-do-for-you/)。也请观看我们的主编【Mike Szczys】的这个 [8 位对 32 位演示](https://hackaday.com/2016/05/11/mike-szczys-ends-8-bit-vs-32-bit-holy-war/)。尽管是五年前的，但它在今天仍然很适用。16 位 MCU 怎么样——旧的英特尔/AMD 嵌入式 80186 处理器，80C196、80C251 或 8051XA 等 8051 的后续产品，65C816、Zilog 的 Z8000、瑞萨 M16C 等 6502 的后续产品。—还有人在使用它们吗？如果是这样，或者如果你现在使用的是 4 位 MCU，请在下面的评论中告诉我们。

 [https://www.youtube.com/embed/jlRAnO1GR0U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jlRAnO1GR0U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢读者[Feinfinger]的提示。