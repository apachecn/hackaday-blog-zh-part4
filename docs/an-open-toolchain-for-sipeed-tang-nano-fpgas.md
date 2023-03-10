# 面向 Sipeed Tang 纳米 FPGAs 的开放式工具链

> 原文：<https://hackaday.com/2022/06/12/an-open-toolchain-for-sipeed-tang-nano-fpgas/>

[Sevan Janiyan]分享了他们在构建开放式 FPGA 工具链方面的研究。具体来说，这是 Sipeed Nano Tang FPGAs 的[开放工具链，](https://www.geeklan.co.uk/?p=2919)这是 Sipeed 从中国提供的相对便宜的产品。官方工具链是专有的，需要你申请一个每年更新的许可证。有一个有限的教育版本，你可以更自由地使用，但当然，这并不一定足以舒适的工作。

这个工具链依赖于 apicula 项目，这是一个对 Gowin FPGA 比特流格式进行逆向工程、重新实现和记录的工作，也是针对 next pnr(FPGA 布局布线的开放工具)的 Gowin 集成。通过 yosys、apicula、nextpnr 和 openFPGAloader 的组合，[Sevan]整理出一组命令，您可以使用这些命令为您的 Nano Tang FPGAs 构建 gateware，而不会受到任何专有限制的阻碍。他们展示了一个基本的 blinkie 演示，以及一个成功操作连接到电路板的并行 LCD 的演示。

FPGAs 开放工具链的可用性一直是一个棘手的问题。想了解开放式 FPGA 工具链吗？由 Tim [Mithro] Ansell 主持的 2019 年 Supercon 讲座将让您快速了解最新情况！

我们感谢[feinfinger(打喷嚏)]与我们分享这个！