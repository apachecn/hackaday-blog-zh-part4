# 如何设计低成本探针示波器

> 原文：<https://hackaday.com/2019/12/16/how-to-design-a-low-cost-probe-oscilloscope/>

[Mark Omo]发来了他关于探针中的示波器的设计的文章，这种示波器有望成为一种低于 100 美元的仪器。

工程中的许多问题都可以通过简单的投资来解决。真正的创新发生在你开始应用约束的时候。Probe-Scope 团队的愿景是拥有 60MHz 带宽和 25Msps 的 USB 示波器。有趣的是，通过在你电脑上的一个空闲 USB 端口上添加另一个探头，你实际上是添加了一个通道。当你买四个的时候，你的价格和普通示波器一样，但是配置更灵活。

该项目也是开源的。当与流行的示波器如 [Rigol](https://hackaday.com/2018/12/19/rigol-mso5000-hacked-features-unlocked/) 相比时，考虑到由于智能开关电路，折扣示波器上的每个通道通常共享多少组件，它具有相当的性能。

该探头基于 ADI 公司的 ADC，其数据由 Lattice FPGA 和 32 位 PIC 微控制器的 tag 团队处理。你可以在他们的 [github](https://github.com/probe-scope) 上看到所有的代码和设计文件。他们的文章包含了对电路的详尽解释。我们希望他们保持项目的势头！