# ORBTrace Effort:专业调试的开放工具

> 原文：<https://hackaday.com/2022/07/26/orbtrace-effort-open-tool-for-professional-debugging/>

今天的微控制器上有一些相当强大的调试工具，如果您的代码神秘地崩溃，很可能有一个调试界面可以让您立即跟踪确切的崩溃情况。可悲的是，这些强大接口的调试工具往往非常昂贵，而且高度专有，因此对爱好者来说并不友好。现在有一个社区驱动的高性能调试平台叫做 [ORBTrace，](https://orbcode.org/orbtrace-mini/)由【mubes】和【zyp】带给我们。

通过并行跟踪，你可以得到一个持续的意识流，每一条精确的指令都由你的 CPU 执行。[mubes]和[zyp]着手开发 Cortex-M 处理器的并行跟踪调试能力。ORBTrace 项目由此诞生。依靠 [Orbuculum 项目的](https://orbcode.org/orbuculum/)软件功能，这个基于 FPGA 的调试器平台可以进行并行跟踪，以及更受欢迎的高速 [SWO 跟踪](https://orbcode.org/orbtrace/using-single-wire-output-when-parallel-trace-isnt-available/)和[方式。](https://orbcode.org/orbuculum/swo-getting-started-with-tooling/) ORBTrace 有潜力成长为一个强大的调试助手工具，其功能足以让任何人受益。当然，它是完全开源的。

ORBTrace 平台有大量未开发的潜力。有[久经沙场考验的 JTAG](https://orbcode.org/orbtrace/orbtrace-for-flashing-fpgas/) 和 SWD，你已经可以和你能想到的所有开放工具一起使用了。然而，FPGA 上也有大量可用资源，甚至包括一个目前未使用的 RISC-V 软核。如果您想为这个调试器添加对任何其他设备家族的支持，那是没有限制的！当然，还有很酷的软件与之配套——例如，[orbmely，](https://github.com/orbcode/orbuculum#orbmortem)它在内存中保留了一个环形指令缓冲区，并向您显示 CPU 停止之前执行的最后一段代码，或者是 [orbstat，](https://orbcode.org/orbuculum/swo-more-instrumentation/)一个用于分析嵌入式代码的工具。

如果你想购买与 Segger 或 Lauterbach 设备同等功能的产品，ORBTrace 并不承诺这一点。相反，它是一个开放的调试工具包项目，硬件[可以购买，](https://store.zyp.no/product/orbtrace-mini)和软件就等着你来控制它。这个项目的社区挂在 [1BitSquared discord 的](https://1bitsquared.com/pages/chat) #orbuculum 频道，和 gateware 的[飞速前进](https://github.com/orbcode/orbtrace/releases)——欢迎你来凑热闹。

当你的目标变大，问题变复杂时，ORBTrace 是一个强大的工具。而且，作为一个社区驱动的实验性努力，我们无疑会看到它带来很大的好处——像 Mooltipass 项目，最初是由 Hackaday 社区成员开发的,,而[仍然在继续发展。](https://hackaday.com/2020/07/23/hands-on-wireless-login-with-the-new-mooltipass-mini-ble-secure-password-keeper/)